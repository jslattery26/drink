<template>
    <img id="test" @click="this.$emit('click')" :src="imgSrc" @mousedown="imgClicked = true;  "
        @mouseup="imgClicked = false; " :height="100" :width="100" />
</template>


<script>
export default {
    data() {
        return {
            imgClicked: false,
            left: new URL(`../assets/keyboards/left.png`, import.meta.url).href,
            leftPressed: new URL(
                `../assets/keyboards/left_pressed.png`,
                import.meta.url
            ).href
        };
    },
    computed: {
        imgSrc: function () {
            return this.imgClicked ? this.leftPressed : this.left;
        }
    },
};
</script>