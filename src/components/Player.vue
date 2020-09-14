<template>
  <div>
    <h1>{{title}}</h1>
    <audio controls preload="metadata">
      <source :src=source />
    </audio>
  </div>
</template>

<script lang='ts'>
import { defineComponent } from 'vue';
// import { defineComponent, PropType } from 'vue';
// import { Sound } from '../models/sound';

export default defineComponent({
  name: 'Player',
  props: {
    // value: {
    //   type: Object as PropType<Sound>,
    //   required: true,
    // },
    title: String,
    source: String,
  },
  data() {
    return {
      // sound: this.value,
    };
  },
});
</script>
