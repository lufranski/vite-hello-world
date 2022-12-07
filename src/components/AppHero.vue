<script>
export default {
    data(){
        return{
            img: 'hero.jpg'
        };
    },
    methods: {
        getImagePath: function (imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    }
};
</script>

<template>
<div>
    <img :src="getImagePath(`../../public/${img}`)" alt="">
</div>
</template>

<style scoped>
img {
    max-width: 90%;
}
</style>