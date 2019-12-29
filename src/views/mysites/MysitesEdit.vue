<template>
  <div id="mysites-edit">
        <VuseBuilder @saved="onSave" :data="site1"/>
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
import newsletter from './sections/forms/newsletter';

Builder.component(section1);
Builder.component(section2);

Builder.component(hero2);
Builder.component(social1);
Builder.component(social2);
Builder.component(social3);
Builder.component(social4);
Builder.component(newsletter);

Vue.use(Builder);

export default {
  components: {

  },
  data() {
    return {
      site1: {
        name: 'Theme 1',
        sections: [hero2, section1, social1, social3, newsletter]
      }
    }
  },
  methods: {
    onSave (builder) {
      // you can use 'preview', 'pwa' or 'json' strings
      // 'json' is the default exporting mode
      builder.export('preview');
    }
  }
}
</script>

<style src='vuse/dist/vuse.css' ></style>
<style src='./style/style.css' ></style>