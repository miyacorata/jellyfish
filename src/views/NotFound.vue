<template>
    <div id="notfound">
        <div class="basic-content" style="text-align: center">
            <h2>Not Found</h2>
            <p>Unfortunately, there is nothing here.</p>
            <p></p>
            <p>
                <router-link to="/">Home</router-link> |
                <a href="https://github.com/miyacorata/jellyfish" target="_blank" rel="noopener">Report to Admin</a>
            </p>
        </div>
    </div>
</template>

<script>
    export default {
        name: "NotFound"
    }
</script>

<style scoped>

</style>