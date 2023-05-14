<template>

    <router-view />

  </template>




  <script setup>

  import 'aos/dist/aos.css';

  import AOS from 'aos';




  AOS.init();

  </script>




  <style scoped>
.v-application{
  display: block !important;
  margin-top: -24px;
}
  /* CSS styles for your component */

  </style>
