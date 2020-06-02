<template>
    <div class="work-card">
        <img :src="image" alt="image">
    </div>
</template>

<script>
    export default {
        name: "WorkCard",
        props: {
            image: {
                type: String,
                required: true
            }
        }
    }
</script>

<style>

</style>