<template>
  <v-app class="main-wrapper-cs">
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
<style>
/* .main-wrapper-cs{
  margin-top: -24px;
} */
.v-application{
  display: block !important;

}
</style>
