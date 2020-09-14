<template>
  <div>
    <player
      :v-for="(music, index) in musics"
      v-bind:source="music.source"
      v-bind:title="music.title"
      :key="index"
    ></player>
    <!-- <player :value="musics"></player> -->
  </div>
</template>

<script lang='ts'>
import { defineComponent } from 'vue';
import Player from '@/components/Player.vue';
import { Sound } from '../models/sound';

export default defineComponent({
  name: 'Playlist',
  components: {
    Player,
  },
  data() {
    return {
      musics: [{
        source: '/AuRa-01-02-Ghost.mp3',
        title: 'Ghost',
        start: 0,
        volume: 1,
        loopable: true,
      }] as Array<Sound>,
    };
  },
});
</script>
