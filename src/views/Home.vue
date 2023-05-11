<template>
  <v-app>
    
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

export default {
  name: 'App',
  components: {
    Footer,
    Header,
    Body
  },

  data: () => ({
    //
  }),
};
</script>
