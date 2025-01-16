<script>
import Vue from 'vue'
import LetItSnow from 'vue-let-it-snow';
Vue.use(LetItSnow);
export default {
  data () {
    return {
      snowConf: {
        windPower : 3,
        speed : 2,
        count : 200,
        size : 1,
        opacity : 0,
      },
      show: false
    }
  },
  mounted () {
    this.show = true
  }
}
</script>
<template>
  <let-it-snow
    v-bind="snowConf"
    :show="show"
  ></let-it-snow>
</template>
