<template>
  <v-app>
    <my-header/>
    <v-content>
      <router-view/>
    </v-content>
    <my-footer />
  </v-app>
</template>

<script>
import Header from './components/Header'
import Footer from './components/Footer'

export default {
  data () {
    return {
      title: 'vue-slider'
    }
  },
  components: {
    'my-header': Header,
    'my-footer': Footer
  },
  name: 'App'
}
</script>
