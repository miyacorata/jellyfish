<template>
    <article class="link-card">
        <div>
            <h3>{{ title }}</h3>
            <p>{{ description }}</p>
            <div class="see-other">
                <div class="tags">
                    <span v-for="tag in tags" :key="tag.value" :class="'tag '+tag.category">{{ tag.value }}</span>
                </div>
                <a class="link" :href="url" target="_blank" rel="noopener">{{ url }}</a>
            </div>

        </div>
    </article>
</template>

<script>
export default {
    name: "LinkCard",
    props: {
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
        },
        url: {
            type: String,
            required: true
        }
    }
}
</script>

<style scoped>
.link-card {
    display: flex;
    align-items: flex-start;
    margin-bottom: 20px;
}
.link-card > div {
    width: 100%;
}
.link-card > div > h3:first-child{
    margin: 0 0 0.3em;
    font-size: 24px;
}
.link-card > div > p{
    margin: 1em 0;
    white-space: pre-wrap;
}
.link-card .see-other{
    margin: 10px 0;
    display: flex;
    justify-content: space-between;
}

.link-card .links {
    text-align: right;
    width: 100%;
}
.link-card a.link {
    display: inline-block;
    margin-left: 10px;
    padding: 2px 8px;
    font-size: 16px;
    text-decoration: none;
    border: solid 1px #61bf99;
    border-radius: 3px;
    transition: background-color .3s, color .3s;
}
.link-card a.link:hover {
    background: #61bf99;
    color: #151515;
}
.link-card a.link:before {
    content: '>';
    font-weight: bold;
    margin-right: 3px;
}
.link-card a.link:hover:before {
    animation: blinker ease 1s infinite;
}

@keyframes blinker {
    0%   { opacity: 1 }
    50%  { opacity: 0.1 }
    100% { opacity: 1 }
}
</style>