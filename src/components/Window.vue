<template>

    <v-window v-model="window" show-arrows>
        <template v-slot:prev="{ props }">
            <LeftArrow @click="props.onClick" />
        </template>
        <template v-slot:next="{ props }">
            <RightArrow @click="props.onClick" />
        </template>
        <v-window-item v-for="n in sprites" :key="n">
            <v-card height="200px" class="d-flex justify-center align-center">
                <v-img class="mr-16 ml-16 mb-6 mt-8" align-center :src="n" color="grey lighten-1" flat tile></v-img>

                <!-- <span class="text-h2">Card {{ n }}</span> -->
            </v-card>
        </v-window-item>

    </v-window>

</template>

<script>
import LeftArrow from "@/components/LeftArrow.vue";
import RightArrow from "@/components/RightArrow.vue";

export default {
    components: {
        LeftArrow,
        RightArrow
    },
    data: () => ({
        length: 16,
        window: 0,
        sprites: [
            new URL(`../assets/sprites/sprite0.gif`, import.meta.url).href,
            new URL(`../assets/sprites/sprite1.gif`, import.meta.url).href,
            new URL(`../assets/sprites/sprite2.gif`, import.meta.url).href,
            new URL(`../assets/sprites/sprite3.gif`, import.meta.url).href,
            new URL(`../assets/sprites/sprite4.gif`, import.meta.url).href,
            new URL(`../assets/sprites/sprite5.gif`, import.meta.url).href,
            new URL(`../assets/sprites/sprite6.gif`, import.meta.url).href,
            new URL(`../assets/sprites/sprite7.gif`, import.meta.url).href,
            new URL(`../assets/sprites/sprite8.gif`, import.meta.url).href,
            new URL(`../assets/sprites/sprite9.gif`, import.meta.url).href,
            new URL(`../assets/sprites/sprite10.gif`, import.meta.url).href,
            new URL(`../assets/sprites/sprite11.gif`, import.meta.url).href,
            new URL(`../assets/sprites/sprite12.gif`, import.meta.url).href,
            new URL(`../assets/sprites/sprite13.gif`, import.meta.url).href,
            new URL(`../assets/sprites/sprite14.gif`, import.meta.url).href
        ]
    })
};
</script>