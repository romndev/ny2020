<script>
export default {
  data: () => ({
    audio: null,
    playing: false,
  }),
  mounted(){
    this.audio = new Audio('audio/6.mp3');
    this.audio.addEventListener('pause', () => { this.playing = false; });
    this.audio.addEventListener('play', () => { this.playing = true; });
  },
  watch:{
    playing(value) {
      if (value) { return this.audio.play(); }
      this.audio.pause();
    },
  },
  methods:{
  },
}
</script>
<template>
  <a @click="playing = !playing" class="btn">
    <span v-if="!playing">Play</span>
    <span v-else>Pause</span>
  </a>
</template>
<style>
.btn{
  color: #fff;
  display: block;
  padding: 20px;
  border: 1px solid #fff;
  border-radius: 10px;
  cursor: pointer;
  margin-top: 34px;
  font-size: 35px;
}
.btn:active {
  color: #fff;
}
</style>
