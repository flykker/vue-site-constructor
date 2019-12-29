<template>
  <div>hfkjgfdsgfkjdsgfkjdsgjdsgfsak</div>
</template>

<script>
import { types } from 'vuse'

export default {
  name: 'Hero1',
  cover: 'img/covers/hero1.png',
  group: 'hero',
  $schema: {
    title: types.Title,
    content: types.Text,
    images: [types.Image],
    button: types.Button,
    classes: types.ClassList
  },
  props: {
    id: {
      type: Number,
      required: true
    }
  }
};
</script>
