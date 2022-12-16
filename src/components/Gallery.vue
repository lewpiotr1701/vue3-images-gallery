<template>
    <v-row>
        <v-col v-for="n in 120" :key="n" cols="6" sm="4" md="2" lg="1">
            <v-card>
                <v-img :src="`https://picsum.photos/500/300?image=${n * 4}`"
                    :lazy-src="`https://picsum.photos/10/6?image=${n * 4}`" aspect-ratio="1" cover>
                    <template v-slot:placeholder>
                        <v-row class="fill-height ma-0" align="center" justify="center">
                            <v-progress-circular indeterminate color="grey-lighten-5"></v-progress-circular>
                        </v-row>
                    </template>
                </v-img>
            </v-card>
        </v-col>
    </v-row>
</template>