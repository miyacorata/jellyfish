<template>
    <div class="head-picture" :style="'background-image: url('+src+')'">
        <h2>{{ title }}</h2>
        <div class="subline" v-if="subline.length">{{ subline }}</div>
    </div>
</template>

<script>
    export default {
        name: "HeadPicture",
        props: {
            src: {
                type: String,
                required: true
            },
            title: {
                type: String,
                required: true
            },
            subline: {
                type: String,
                default: ''
            }
        }
    }
</script>

<style scoped>
    .head-picture{
        width: 100%;
        text-align: center;
        background-repeat: no-repeat;
        background-position: center;
        background-color: black;
        background-size: 100vw auto;
        padding: 5px 0;
        box-shadow: inset 0 0 10px black;
        text-shadow: 0 0 15px black, 0 0 15px black;
    }

    h2{
        font-size: 30px;
        margin: 10px auto 5px;
    }
    div.subline{
        font-size: 18px;
        margin: 5px auto 10px;
    }

    img {
        width: 100%;
        height: 120px;
        object-fit: cover;
        box-shadow: inset 0 0 15px black;
        object-position: center;
    }
</style>