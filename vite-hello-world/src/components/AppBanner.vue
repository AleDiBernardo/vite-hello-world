<script>
export default{
    data(){
        return{
            image: "screenshot.png"
        }
    },
    methods: {
        getImagePath(imageName){
            return new URL(`../assets/img/${imageName}`, import.meta.url).href;
        }
    }
}
</script>

<template>
    <div class="banner">
        <img :src="getImagePath(image)" alt="">
    </div>
</template>

<style>
    .banner  {
        width: 100%;
    }

    img {
        max-width: 100%;
    }
</style>