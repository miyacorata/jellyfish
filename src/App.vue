<template>
    <div id="app">
        <header>
            <h1>
                <img src="https://github.com/miyacorata.png" alt="miyacorata">
                miyacorata.net
            </h1>
            <div id="nav">
                <router-link to="/">Home</router-link>
                <router-link to="/about">About</router-link>
                <router-link to="/works">Works</router-link>
                <router-link to="/links">Links</router-link>
                <a href="https://miyacorata.hatenablog.com" target="_blank">Blog</a>
            </div>
        </header>
        <main>
            <transition mode="out-in">
                <router-view/>
            </transition>
        </main>
        <footer>
            <p id="app-info">{{ host + ' - ' + appName + ' Ver' + version }}</p>
            <p id="footer-text">
                And it shall be bestowed upon you,
                the Star which you have longed for─
            </p>
        </footer>
    </div>
</template>

<script>
    import info from '../package.json'

    export default {
        data() {
            return {
                host: location.hostname,
                appName: info.name.substr(0,1).toUpperCase() + info.name.substr(1),
                version: info.version
            }
        }
    }
</script>

<style>
    body {
        margin: 0;
        padding: 0;
        background: #151515;
        overflow-y: scroll;
    }

    #app {
        position: relative;
        font-family: 'Noto Serif', 'Noto Serif JP', sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        color: floralwhite;
        min-height: 100vh;
    }
    main {
        padding-bottom: 110px;
    }

    header{
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
        flex-wrap: wrap;
        padding: 15px;
        height: 60px;
        box-sizing: border-box;
    }

    header > h1 {
        font-size: 20px;
        margin: 0;
    }

    header > h1 > img:first-child {
        height: 1.4em;
        vertical-align: bottom;
        margin-right: 10px;
        border-radius: 2px;
    }

    #nav {
        padding-left: 15px;
    }
    #nav:before {
        content: '/';
    }

    #nav a {
        font-weight: bold;
        text-decoration: none;
        color: #61bf99;
        margin-left: 15px;
        transition: color .4s;
    }

    #nav a.router-link-exact-active {
        color: #fafafa;
        text-decoration: none;
        position: relative;
    }
    #nav a.router-link-exact-active::after{
        content: '▼';
        transform: scale(0.5);
        position: absolute;
        left: 0; right: 0;
        bottom: -18px;
    }

    .v-enter-active {
        transition: opacity .8s;
    }
    .v-leave-active {
        transition: opacity .2s;
    }
    .v-enter, .v-leave-to {
        opacity: 0;
    }

    footer {
        position: absolute;
        bottom: 0;
        width: 100%;
        height: 70px;
        margin-top: 40px;
        padding: 20px 0;
        text-align: center;
        font-size: 15px;
    }

    p {
        margin: 0.5em 0;
    }

    footer > p#footer-text {
        font-size: 13px;
        font-style: italic;
        color: gray;
    }

    .basic-content {
        max-width: 1000px;
        margin: 0 auto;
    }

    a {
        color: #61bf99;
    }

    .tag {
        display: inline-block;
        margin-right: 10px;
        padding: 0 8px 0 6px;
        border-radius: 2px;
        border-left: solid 5px blue;
        background: floralwhite;
        color: #151515;
    }

    .tag.content {
        border-left-color: orange;
    }
    .tag.tech {
        border-left-color: deepskyblue;
    }

    p.notes {
        background: rgba(99,99,99,0.3);
        border-radius: 4px;
        padding: 10px;
        margin: 1.2em 0;
    }
</style>
