<template>
  <v-app :theme="theme">

    <SideBar @toggle-theme="toggleTheme" :themeProp="theme" />

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
  },
  data() {
    return {
      theme: 'light'
    }
  },
  methods: {
    toggleTheme(themeValue) {
      this.theme = this.theme === 'light' ? 'dark' : 'light'
    }
  }

}
</script>