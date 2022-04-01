<template>
  <v-app>
    <nav-bar></nav-bar>
    <v-main class="grey lighten-5">
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>

import navBar from '@/components/NavBar.vue'

export default {
  name: 'App',
  components: {
    navBar
  },
  data: () => ({
    //
  }),
};
</script>

<style>
.margin10 {
  margin: 10px;
  margin-top: 20px;
}
</style>
