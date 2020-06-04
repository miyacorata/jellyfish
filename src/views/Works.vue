<template>
    <div id="about">
        <HeadPicture title="Works"
                     src="https://files.miyacorata.net/images/jellyfish/subway.jpg"
                     subline="これまでの制作物"/>
        <div class="basic-content">
            <h2>Websites</h2>
            <WorkCard v-for="work in works.websites" :key="work.name" :image="work.image" :title="work.name"
                      :description="work.description" :tags="work.tags" :links="work.links" :github="work.github"/>
        </div>
    </div>
</template>

<script>
    import HeadPicture from "../components/HeadPicture";
    import WorkCard from "../components/WorkCard";
    import works from "../datas/works.json";

    export default {
        name: "Works",
        components: {WorkCard, HeadPicture},
        data: ()=>{
            return {
                works: works
            }
        }
    }
</script>

<style scoped>

</style>