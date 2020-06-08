<template>
    <div id="hello">
        <h1>{{ msg }}</h1>
        <p style="font-style: italic">
            miyacorata.net へようこそ
        </p>
        <h3>Contents</h3>
        <ul>
            <li><router-link to="/about">About</router-link></li>
            <li><router-link to="/works">Works</router-link></li>
            <li><a href="https://miyacorata.hatenablog.com" target="_blank">Blog</a></li>
        </ul>
        <h3>Recent Tweets</h3>
        <div>
            <Timeline id="miyacorata" sourceType="profile" :options="{width:400,height:600,theme:'dark',dnt:true}"></Timeline>
        </div>
    </div>
</template>

<script>
    import {Timeline} from 'vue-tweet-embed'

    export default {
        components: {Timeline},
        name: 'HelloWorld',
        props: {
            msg: String
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    h3 {
        margin: 40px 0 10px;
    }
    ul {
        list-style-type: none;
        padding: 0;
    }
    li {
        display: inline-block;
        margin: 0 10px;
    }
</style>
