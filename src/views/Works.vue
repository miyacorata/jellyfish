<template>
    <div id="about">
        <HeadPicture title="Works"
                     src="https://files.miyacorata.net/images/jellyfish/subway.jpg"
                     subline="これまでの制作物"/>
        <div class="basic-content">
            <h2>Websites</h2>
            <WorkCard image="https://files.miyacorata.net/images/jellyfish/mlp.jpg"
                      title="MillionLivePortal"
                      description="アイドルマスターミリオンライブ！の非公式DB＆ポータルサイト"
                      :tags="[
                          {
                              category: 'content',
                              value: 'THE IDOLM@STER'
                          },
                          {
                              category: 'tech',
                              value: 'PHP'
                          },
                          {
                              category: 'tech',
                              value: 'Laravel'
                          }
                      ]"/>
        </div>
    </div>
</template>

<script>
    import HeadPicture from "../components/HeadPicture";
    import WorkCard from "../components/WorkCard";
    export default {
        name: "Works",
        components: {WorkCard, HeadPicture}
    }
</script>

<style scoped>

</style>