# vue-image-card-library

This is a set of `Vue` Image card components for special purposes. Each components come with `props` and `slots` for easy customization. The CSS animation make it awesome, thanks to the developer community.

## vue-profile-Card

_VueProfileCard_ is a `CSS` animated **Image Card** with background animation.

[Demo](http://bulma-vuejs-profile.vercel.app/)

### Props and slots

This component come with a single prop `img`, which can be used to pass a image url and an `alt` tag. This prop is an object.

```
img: {
      type: Object,
      default: new Object({
        src:
          "https://images.unsplash.com/photo-1532123675048-773bd75df1b4?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=500&q=60",
        alt: "images",
      }),
    },
```

The `slot details` can be used to _add set of social icons or single paragraph or heading of your choice_.

```<template>
  <div id="app">
    <vue-profile-card >
     <template slot="details">
                  <h1 class="is-size-5">Web Developer</h1>
                  <span class="icon  ">
                <i>
                 <a :href="`${fb}`"> <v-icon name="md-facebook" scale="1.5" /></a>
                </i>
                <i>
                  <a :href="`${gh}`"> <v-icon name="oi-octoface" scale="1.5" /></a>
                </i>
                <i>
                  <a :href="`${tw}`"> <v-icon name="bi-twitter" scale="1.5"/></a>
                </i> <i>
                 <a :href="`${wp}`">  <v-icon name="fa-wordpress"  scale="1.5"/></a>
                </i></span>
      </template>
      </vue-profile-card>
  </div>
</template>

<script>

import VueProfileCard from '@manojap/vue-profile-card'
export default {
  name: "App",
  components: {
    VueProfileCard
  },
};
</script>
```

## vue-mini-bio

_VueMiniBio_ is a Image card with a Opening panel (hover effect) which can be used to show bio with social (customizable)

### slots

`img` slot can be used to style the main image according to your needs and the `detail` slot help to set the content

```
 <slot name="img">
        <div class="image">
          <img
            src="https://images.unsplash.com/photo-1574100004472-e536d3b6bacc?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=334&q=80"
          />
        </div>
      </slot>

      <slot name="details">
        <h1>Someone nonsense<br /><span>team leader</span></h1>
        <p>
          Lorem ipsum is simple dummy text on the printing and typesetting industry.
        </p>
        <ul>
          <li>
            <a href="#"><i class="fa fa-facebook" aria-hidden="true"></i></a>
          </li>
          <li>
            <a href="#"><i class="fa fa-twitter" aria-hidden="true"></i></a>
          </li>
          <li>
            <a href="#"><i class="fa fa-google-plus" aria-hidden="true"></i></a>
          </li>
          <li>
            <a href="#"><i class="fa fa-linkedin" aria-hidden="true"></i></a>
          </li>
          <li>
            <a href="#"><i class="fa fa-instagram" aria-hidden="true"></i></a>
          </li>
        </ul>
      </slot>
```

### Usage

```
import {vueMiniBio} from '@manojap/vue-img-cards';
import Vue from 'vue';

export default Vue.extend({
  components: { vueMiniBio },
  name: 'App',
});
</script>

<template>
  <div id="app">
    <vue-mini-bio/>
  </div>
</template>

```

## License

MIT © [manojap](https://github.com/manojap)
