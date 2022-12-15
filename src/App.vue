<template>
  <v-app theme="dark">

    <SideBar />

    <v-main>

    </v-main>

  </v-app>
</template>

<script>
import SideBar from './components/SideBar.vue'

export default {
  name: 'App',
  components: {
    SideBar
  }

}
</script>