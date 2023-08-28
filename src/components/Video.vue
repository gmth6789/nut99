<template>
  <nut-video :source="source" :options="options"></nut-video>
</template>
<script lang="ts">
  import { toRefs, reactive } from 'vue';
  export default {
    setup() {
      const state = reactive({
        source: {
          src: 'https://storage.jd.com/about/big-final.mp4?Expires=3730193075&AccessKey=3LoYX1dQWa6ZXzQl&Signature=ViMFjz%2BOkBxS%2FY1rjtUVqbopbJI%3D',
          type: 'video/mp4'
        },
        options: {
          autoplay: true,
          muted: true,
          controls: true
        }
      });

      return { ...toRefs(state) };
    }
  };
</script>
