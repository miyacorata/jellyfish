<template>
    <div id="home">
        <div class="home-title">
            <img src="https://files.miyacorata.net/images/jellyfish/mahiru.png" alt="mahiru">
            <div>
                <h1>miyacorata.net</h1>
                <div class="subline">The website of K Miyano</div>
            </div>
        </div>
        <HelloWorld msg="Welcome to miyacorata.net"/>
    </div>
</template>

<script>
    // @ is an alias to /src
    import HelloWorld from '@/components/HelloWorld.vue'

    export default {
        name: 'Home',
        components: {
            HelloWorld
        }
    }
</script>

<style>
    #home {
        text-align: center;
    }
    .home-title{
        width: 100%;
        display: flex;
        position: relative;
        justify-content: center;
        align-items: center;
        text-align: left;
        background-color: white;
        padding: 0;
        color: #151515;
        overflow: hidden;
    }
    .home-title::after{
        content: '';
        position: absolute;
        box-shadow: inset 0 0 10px black;
        top: 0; bottom: 0; left: 0; right: 0;
        margin: 0 -10px;
        overflow: hidden;
    }
    .home-title > img:first-child{
        height: 200px;
        padding-top: 10px;
        margin-right: 40px;
        margin-left: -30px;
    }
</style>
