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
import Body from '@/components/Body.vue'

export default {
  name: 'Home',
  components: {
    Header,
    Body
  },
};
</script>
