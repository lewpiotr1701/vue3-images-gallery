<template>
    <v-card class="ma-4 pa-2">
        <v-row>
            <v-col v-for="n in 24" :key="n" cols="6" sm="4" md="2" lg="1">
                <v-hover v-slot="{ isHovering, props }">
                    <v-card :elevation="isHovering ? 12 : 2" v-bind="props"
                        @click="copyUrl(`https://picsum.photos/500/300?image=${n * 4}${color ? '' : '&grayscale'}`)">
                        <v-img :src="`https://picsum.photos/500/300?image=${n * 4}${color ? '' : '&grayscale'}`"
                            :lazy-src="`https://picsum.photos/10/6?image=${n * 4}${color ? '' : '&grayscale'}`"
                            aspect-ratio="1" cover>
                            <template v-slot:placeholder>
                                <v-row class="fill-height ma-0" align="center" justify="center">
                                    <v-progress-circular indeterminate color="grey-lighten-5"></v-progress-circular>
                                </v-row>
                            </template>
                        </v-img>
                    </v-card>
                </v-hover>
            </v-col>
        </v-row>
    </v-card>
</template>

<script>
export default {
    name: 'Gallery',
    props: ['color'],
    methods: {
        async copyUrl(url) {
            await navigator.clipboard.writeText(url)
        }
    }
}
</script>