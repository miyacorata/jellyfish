<template>
    <article class="work-card">
        <img :src="image" alt="image">
        <div>
            <h3>{{ title }}</h3>
            <p>{{ description }}</p>
            <div class="tags">
                <span v-for="tag in tags" v-bind:key="tag.value" :class="'tag '+tag.category">{{ tag.value }}</span>
            </div>
        </div>
    </article>
</template>

<script>
    export default {
        name: "WorkCard",
        props: {
            image: {
                type: String,
                required: true
            },
            title: {
                type: String,
                required: true
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
            }
        }
    }
</script>

<style>
    .work-card {
        display: flex;
        align-items: flex-start;
    }
    .work-card > img:first-child{
        width: 250px;
        box-sizing: border-box;
        margin-right: 20px;
    }
    .work-card > div > h3:first-child{
        margin: 0 0 0.3em;
        font-size: 24px;
    }
    .work-card > div > p{
        margin: 1em 0;
    }

    .tag {
        display: inline-block;
        margin-right: 10px;
        padding: 0 5px;
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
</style>