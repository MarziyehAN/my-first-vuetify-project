<template>
  <v-app :style="{background:$vuetify.theme.themes.light.colors.primary}">
    <NavBare/>
    <v-main>
        <v-container fluid>
            <p class="mb-6">This page is Developing...</p>
            <v-carousel>
                <v-carousel-item
                    src="car (1).jpg"
                    cover
                ></v-carousel-item>

                <v-carousel-item
                    src="car (2).jpg"
                    cover
                ></v-carousel-item>

                <v-carousel-item
                    src="car (3).jpg"
                    cover
                ></v-carousel-item>
                </v-carousel>

        </v-container>
    </v-main>
  </v-app>
</template>

<script>
import NavBare from '@/components/NavBare.vue';

export default {
    components: { NavBare }
}
</script>

<style>

</style>