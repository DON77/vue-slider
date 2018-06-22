<template>
  <v-app>
    <Header/>
    <v-content>
      <router-view/>
    </v-content>
    <Footer />
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
    Header,
    Footer
  },
  name: 'App'
}
</script>
