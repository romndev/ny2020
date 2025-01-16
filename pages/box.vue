<template>
  <div class="container">
    <div>
      <h1 class="title">Надень Airpods</h1>
      <h1 class="title">Нажми на Play</h1>
      <h1 class="title">Прибавь громкость</h1>
      <h1 class="title">Закрой глаза</h1>
      <Player v-model="play" />
      <NuxtLink to="/" style="margin-top: 20px;
    display: block;
    color: #fff;
    text-decoration: none;">Назад</NuxtLink>
    </div>
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

.links {
  padding-top: 15px;
}
</style>
