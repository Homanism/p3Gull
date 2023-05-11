<template>
  <v-app>
    <NavBar />
    <Header />
    <v-main>
      <router-view />
      <Body />
    </v-main>
    <Footer />
  </v-app>
</template>

<script >
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'
import Body from '@/components/Body.vue'
import NavBar from '@/components/NavBar.vue'
export default {
  name: 'App',
  components: {
    NavBar,
    Footer,
    Header,
    Body
  },

  data: () => ({
    //
  }),
};
</script>
