<template>
  <v-app>
    <v-main>
      <Navbar />
      <Landing />
    </v-main>
  </v-app>
</template>

<script lang="ts">
import Navbar from './components/Navbar.vue'
import Landing from './components/Landing.vue'


export default {
  name: 'App',
}

</script>
