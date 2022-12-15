<template>
    <v-navigation-drawer expand-on-hover rail>

        <v-list>
            <v-list-item prepend-avatar="https://randomuser.me/api/portraits/women/85.jpg" title="Sandra Adams"
                subtitle="sandra_a88@gmailcom"></v-list-item>
        </v-list>

        <v-divider></v-divider>

        <v-list density="compact" nav>
            <v-list-item prepend-icon="mdi-image" title="Color images" value="color"></v-list-item>
            <v-list-item prepend-icon="mdi-dialpad" title="Gray images" value="grayColor"></v-list-item>
        </v-list>
    </v-navigation-drawer>
</template>

<script>
export default {
    name: 'SideBar'
}
</script>