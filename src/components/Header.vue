8<template>
  <div class="header__div">
    <NavBar /> <br><br><br><br>
    <v-img src="https://p3.no/wp-content/uploads/2022/11/P3Gull_aaretsartist.png"></v-img>
  </div>
</template>
<script>
import NavBar from '@/components/NavBar.vue'

export default {
  name: 'Header',
  components: {
    NavBar,
  },

  data: () => ({
    //
  }),
};
  //
</script>
<style>
.header__div{
  /* margin-left: 6%; */
  margin-top: -8%;
}

</style>
