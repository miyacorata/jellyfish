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
                    <div class="links">
                        <github-button href="https://github.com/miyacorata" data-size="large" aria-label="Follow @miyacorata on GitHub">miyacorata</github-button>
                        <a href="https://twitter.com/miyacorata" class="twitter" target="_blank" rel="noopener"><i class="fab fa-twitter"></i>@miyacorata</a>
                    </div>
                    <h3 style="margin-top: 30px">Skills</h3>
                    <p>HTML5, PHP (contain Laravel), CSS (contain Bulma), JavaScript (Vanilla.js, Vue.js)</p>
                    <h3>Favorite Contents</h3>
                    <p>THE IDOLM@STER (MillionLive), 少女☆歌劇 レヴュースタァライト, and more...</p>
                    <h3>Favorite activities</h3>
                    <p>Travelling, Driving, Photography, and more...</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import HeadPicture from "../components/HeadPicture";
    import GithubButton from 'vue-github-button';
    export default {
        components: {HeadPicture, GithubButton}
    }
</script>

<style scoped>
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
    #profile .links > a, #profile .links > span {
        display: inline-block;
        vertical-align: top;
        margin-right: 10px;
    }
    #profile .links > a {
        display: inline-block;
        vertical-align: top;
        padding: 2px 8px;
        font-size: 16px;
        text-decoration: none;
        border: solid 1px #61bf99;
        border-radius: 3px;
        transition: background-color .3s, color .3s;
    }
    #profile .links > a > .fab {
        margin-right: 3px;
    }
    #profile .links > a:hover {
        background: #61bf99;
        color: #151515;
    }
    #profile .links > a.twitter {
        background: #00acee;
        border-color: #00acee;
        color: white;
    }
</style>
