<template>
  <div class="container">
    <div>
      <Logo />
      <div class="links">
        <NuxtLink
          to="box"
          class="button--grey"
        >
          Открыть подарок
        </NuxtLink>
      </div>
    </div>
    <!--Player v-model="play" /-->
  </div>
</template>

<script>
import Player from "~/components/Player";
import Vue from 'vue';
import vueAwesomeCountdown from 'vue-awesome-countdown';
Vue.use(vueAwesomeCountdown, 'countdown')
import Countdown from 'vue-awesome-countdown'
export default {
  data: () => ({
    play: false,
  }),
  components: {
    Player,
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 40px;
  color: #ffffff;
  letter-spacing: 1px;
  margin-top: 20px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.button--grey{
  border-color: white;
  margin-top: 20px;
  color: #fff;
  font-size: 29px;
}

.links {
  padding-top: 15px;
}
</style>
