<template>
    <v-navigation-drawer expand-on-hover rail>

        <v-list>
            <v-list-item prepend-avatar="https://randomuser.me/api/portraits/women/85.jpg" title="Sandra Adams"
                subtitle="sandra_a88@gmailcom"></v-list-item>
        </v-list>

        <v-divider></v-divider>

        <v-list density="compact" nav>
            <v-list-item :prepend-icon="theme === 'light' ? 'mdi-weather-sunny' : 'mdi-weather-night'"
                title="Toggle Theme" value="theme" @click="onClickToggle"></v-list-item>
            <v-list-item prepend-icon="mdi-image" title="Color images" value="color"
                @click="onClickColor(true)"></v-list-item>
            <v-list-item prepend-icon="mdi-dialpad" title="Gray images" value="grayColor"
                @click="onClickColor(false)"></v-list-item>
        </v-list>
    </v-navigation-drawer>
</template>

<script>
export default {
    name: 'SideBar',
    props: {
        currentTheme: String,
        required: true
    },
    // emits: [onClickToggle, onClickColor],
    data() {
        return {
            theme: this.currentTheme
        }
    },
    methods: {
        onClickToggle() {
            this.theme = this.theme === 'light' ? 'dark' : 'light'

            this.$emit('toggleTheme', this.theme)
        },
        onClickColor(color) {
            this.$emit('selectColor', color)
        }
    }
}
</script>