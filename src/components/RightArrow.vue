<template>
    <img id="test" @click="this.$emit('click')" :src="imgSrc" @mousedown="imgClicked = true;  "
        @mouseup="imgClicked = false; " :height="100" :width="100" />
</template>


<script>
export default {
    data() {
        return {
            imgClicked: false,
            right: new URL(`../assets/keyboards/right.png`, import.meta.url).href,
            rightPressed: new URL(
                `../assets/keyboards/right_pressed.png`,
                import.meta.url
            ).href
        };
    },
    computed: {
        imgSrc: function () {
            return this.imgClicked ? this.rightPressed : this.right;
        }
    },
};
</script>