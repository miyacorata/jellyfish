<template>
    <article class="work-card">
        <img :src="image" alt="image">
        <div>
            <h3>{{ title }}</h3>
            <p>{{ description }}</p>
            <div class="tags">
                <span v-for="tag in tags" :key="tag.value" :class="'tag '+tag.category">{{ tag.value }}</span>
            </div>
            <div class="see-other">
                <div class="github">
                    <github-button v-if="github" :href="'https://github.com/'+github" data-size="large"
                                   data-show-count="true" :aria-label="'Star '+github+' on GitHub'">View on GitHub</github-button>
                </div>
                <div class="links">
                    <a v-for="link in links" :key="link.name" :href="link.url" target="_blank" rel="noopener">{{ link.name }}</a>
                </div>
            </div>
        </div>
    </article>
</template>

<script>
    import GithubButton from 'vue-github-button'

    export default {
        name: "WorkCard",
        components: {
            GithubButton
        },
        props: {
            image: {
                type: String,
                required: true
            },
            title: {
                type: String,
                required: true
            },
            github: {
                type: String,
                default: null
            },
            description: {
                type: String,
                required: true
            },
            tags: {
                type: Array,
                default: () => {
                    return []
                }
            },
            links: {
                type: Array,
                default: () => {
                    return []
                }
            }
        }
    }
</script>

<style>
    .work-card {
        display: flex;
        align-items: flex-start;
        margin-bottom: 20px;
    }
    .work-card > img:first-child{
        width: 250px;
        box-sizing: border-box;
        margin-right: 20px;
    }
    .work-card > div {
        width: 100%;
    }
    .work-card > div > h3:first-child{
        margin: 0 0 0.3em;
        font-size: 24px;
    }
    .work-card > div > p{
        margin: 1em 0;
        white-space: pre-wrap;
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

    .work-card .see-other {
        margin: 10px 0;
        display: flex;
    }
    .work-card .links {
        text-align: right;
        width: 100%;
    }
    .work-card .links > a {
        display: inline-block;
        vertical-align: top;
        margin-left: 10px;
        padding: 2px 8px;
        font-size: 16px;
        text-decoration: none;
        border: solid 1px #61bf99;
        border-radius: 3px;
        transition: background-color .3s, color .3s;
    }
    .work-card .links > a:hover {
        background: #61bf99;
        color: #151515;
    }
    .work-card .links > a:before {
        content: '>';
        font-weight: bold;
        margin-right: 3px;
    }
    .work-card .links > a:hover:before {
        animation: blinker ease 1s infinite;
    }
    .v-leave-active .work-card .github > span{
        opacity: 0;
    }
    @keyframes blinker {
        0%   { opacity: 1 }
        50%  { opacity: 0.1 }
        100% { opacity: 1 }
    }
</style>