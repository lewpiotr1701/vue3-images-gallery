<template>
  <v-app :theme="theme">
    <SideBar @toggle-theme="toggleTheme" :current-theme="theme" />
    <v-main>
      <Gallery />
    </v-main>
  </v-app>
</template>

<script>
import SideBar from './components/SideBar.vue'
import Gallery from './components/Gallery.vue'

export default {
  name: 'App',
  components: {
    SideBar,
    Gallery
  },
  data() {
    return {
      theme: 'dark'
    }
  },
  methods: {
    toggleTheme(themeValue) {
      this.theme = themeValue
    }
  }

}
</script>