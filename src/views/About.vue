<template>
    <div id="about">
        <HeadPicture title="About"
                     src="https://files.miyacorata.net/images/jellyfish/ohorikoen.jpg"
                     subline="miyacorata.net について"/>
        <div class="basic-content">
            <h2>Profile</h2>
            <div id="profile">
                <img src="https://github.com/miyacorata.png" alt="miyacorata">
                <div>
                    <p class="name">宮野 慧<span class="screenname">miyacorata</span></p>
                    <p>
                        佐賀県佐賀市在住 久留米高専プログラミングラボ部所属の下手の横好き趣味グラマ
                    </p>
                    <p>
                        『アイドルマスター』シリーズや『少女☆歌劇 レヴュースタァライト』などを追っかけています
                    </p>
                    <p>
                        プログラミングの他クルマでのドライブや「こけし」と名付けている作図もといおえかきを趣味にしています
                    </p>
                    <h3>Skills</h3>
                    <p>HTML5, PHP (contain Laravel), CSS (contain Bulma), JavaScript (Vanilla.js, Vue.js)</p>

                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import HeadPicture from "../components/HeadPicture";
    export default {
        components: {HeadPicture}
    }
</script>

<style>
    #profile {
        display: flex;
        align-items: flex-start;
    }
    #profile > img:first-child {
        width: 170px;
        border-radius: 3px;
        margin-right: 30px;
    }
    #profile .name {
        font-size: 30px;
        margin-top: 0;
    }
    #profile .name .screenname {
        font-size: 20px;
        margin-left: 20px;
        color: gray;
    }
</style>
