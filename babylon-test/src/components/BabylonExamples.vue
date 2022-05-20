<template>
  <div class="main">
    <h3>
    Babylon Examples
  </h3>
  <canvas></canvas>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import { BasicScene } from '@/classes/BasicScene';

export default defineComponent({
  name: 'BabylonExamples',
  mounted(){
    // eslint-disable-next-line @typescript-eslint/no-non-null-assertion
    const canvas = document.querySelector("canvas")!;
    new BasicScene(canvas)
  }
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
canvas {
    -webkit-touch-callout: none;
    -webkit-user-select: none;
    -khtml-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none;
    outline: none;
    -webkit-tap-highlight-color: rgba(255, 255, 255, 0); /* mobile webkit */
}

.main {
  background-color: black;
  height: 100vh;
  width: 100%;
  margin: 0;
  padding-top: 5vh;
}

h3 {
  color: white;
  font-weight: 600;
  margin: 0;
  padding-bottom: 5vh;
}

canvas {
  height: 70%;
  width: 70%;
  filter: drop-shadow(7px 4px 2px black)
}
</style>
