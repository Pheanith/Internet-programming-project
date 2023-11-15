<template>
    <div class="promotion" :style="{backgroundColor: colorBackground}">
        <p class="desc">{{ description }}</p>
        <Button class="btn" :style="{backgroundColor: btnbgcolor}">
                <div class="text">{{ btntext }}</div>
                <i class="uil uil-arrow-right"></i>
        </Button>
        <img :src="productImages" alt="onions">
    </div>
</template>
<script>
import Button from "./button.vue";
export default {
    name: "Promotion",
    componet: {
        Button,
    },
    props: {
        colorBackground: String,
        productImages: String,
        description: String,
        btnbgcolor: String,
        btntext: String,
    }
}
</script>
<style>
    .promotion{
        width: 500px;
        height: 300px;
        border-radius: 10px;
        position: relative;
        display: flex;
        justify-content: center;
        align-content: center;
    }
    .desc{
        width: 50%;
        height: 100%;
        color:  #253D4E;
        font-size: 24px;
        font-weight: 700;
        font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
        padding: 10%  0 0 8%;
    }
    img{
        position: relative;
        width: 50%;
        height: 200px;
        border-radius: 0 0 10px 10px;
        margin: 50px 0 0 0;
        display: flex;
        object-fit: contain;
        mix-blend-mode: multiply;
    }
    .btn{
        position: absolute;
        top: 200px;
        left: 42px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 8px 15px;
    }
    .text{
        font-size: 20px;
        font-family: Verdana, Geneva, Tahoma, sans-serif;
        color: #fff;
        font-size: 14px;
    }
    .uil{
        font-size: 15px;
        color: #fff;
    }
</style>