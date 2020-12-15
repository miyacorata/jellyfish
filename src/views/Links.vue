<template>
    <div id="links">
        <HeadPicture title="Links"
                     src="https://files.miyacorata.net/images/jellyfish/ohorikoen.jpg"
                     subline="リンク集" />
        <div class="basic-content">
            <h2>Links</h2>
            <p class="notes">miyacorata.netが運営ないしお手伝いしているウェブサイトのうちWorksに掲載していないものを掲載しています。</p>
            <LinkCard v-for="link in links.links" :key="link.name" :title="link.name"
                      :description="link.description" :tags="link.tags" :url="link.url"/>
        </div>
    </div>
</template>

<script>
import HeadPicture from "@/components/HeadPicture";
import LinkCard from "@/components/LinkCard";
import links from "@/datas/links.json";

export default {
    name: "Links",
    components: {LinkCard, HeadPicture},
    data: () => {
        return {
            links: links
        }
    }
}
</script>

<style scoped>

</style>