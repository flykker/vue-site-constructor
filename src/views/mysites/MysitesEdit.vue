<template>
  <div id="mysites-edit">
        <VuseBuilder />
  </div>
</template>

<script>
import Vue from "vue"
// import VuseRenderer from "vuse"
import Builder from 'vuse'
import './style/_demo.styl';

import section1 from './sections/section/section1.vue';
import section2 from './sections/section/section2.vue';


import hero2 from './sections/hero/hero2';
import social1 from './sections/social/social1';
import social2 from './sections/social/social2';
import social3 from './sections/social/social3';
import social4 from './sections/social/social4';

Builder.component(section1);
Builder.component(section2);

Builder.component(hero2);
Builder.component(social1);
Builder.component(social2);
Builder.component(social3);
Builder.component(social4);

Vue.use(Builder);

export default {
  components: {
  },
  data() {
    return {
    }
  }
}
</script>

<style src='vuse/dist/vuse.css' ></style>