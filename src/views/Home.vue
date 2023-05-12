<template>
  <v-app>
    <Header />
      <Body />
    <Footer />
  </v-app>
</template>

<script >
import Header from '../components/Header.vue'
import Footer from '../components/Footer.vue'
import Body from '../components/Body.vue'
export default {
  name: 'Home',
  components: {
    Header,
    Body,
    Footer
  },

};
</script>
