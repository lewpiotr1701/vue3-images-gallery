<template>
  <v-app :theme="theme">
    <SideBar @toggle-theme="toggleTheme" @select-color="selectColor" :current-theme="theme" />
    <v-main>
      <Gallery :color="color" />
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
      theme: 'dark',
      color: true
    }
  },
  methods: {
    toggleTheme(themeValue) {
      this.theme = themeValue
    },
    selectColor(color) {
      this.color = color
      console.log(this.color)
    }
  }

}
</script>