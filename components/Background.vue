<script>
import Granim from "granim";

export default {
  mounted(){
    var granimInstance = new Granim({
      element: '#granim-canvas',
      name: 'granim',
      opacity: [1, 1],
      states : {
        "default-state": {
          gradients: [
            ['#834D9B', '#D04ED6'],
            ['#1CD8D2', '#93EDC7']
          ]
        }
      }
    });
  }
}
</script>
<template>
  <canvas id="granim-canvas"></canvas>
</template>
<style>
#granim-canvas {
  position: absolute;
  display: block;
  width: 100%;
  height: 100%;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: -1;
}
</style>
