<script>
import {defineComponent} from 'vue'
import { mapState } from 'vuex'
export default defineComponent({
  name: "CounterVuex",
  computed: {
    countComputed() {
      return this.$store.state.count
    },
    ...mapState(['count'])
    /*
    ...mapState({
      count: state => state.count,
      lastMutation: state => state.lastMutation
    })

     */
  }
})
</script>

<template>
  <h1>Counter - Vuex</h1>
  <h2>Direct access: {{ $store.state.count }}</h2>
  <h2>Computed: {{ countComputed }}</h2>
  <h1>mapState</h1>
  <h2>mapState: {{ count }}</h2>
  <!--<h2>lastMutation: {{ lastMutation }}</h2>-->
</template>