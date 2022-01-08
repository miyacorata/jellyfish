<template>
    <div id="about">
        <HeadPicture title="About"
                     src="https://files.mrapid.org/images/jellyfish/ohorikoen.jpg"
                     subline="miyacorata.net について"/>
        <div class="basic-content">
            <h2>Profile</h2>
            <div id="profile">
                <img src="https://github.com/miyacorata.png" alt="miyacorata">
                <div>
                    <p class="name">宮野 慧<span class="screenname">miyacorata</span></p>
                    <p>
                        佐賀県佐賀市在住 フリーター兼下手の横好き趣味グラマ
                    </p>
                    <p>
                        『少女☆歌劇 レヴュースタァライト』、『アサルトリリィ』などを追っかけています
                    </p>
                    <p>
                        プログラミングの他クルマでのドライブや「こけし」と名付けている作図もといおえかきを趣味にしています
                    </p>
                    <div class="links">
                        <github-button href="https://github.com/miyacorata" data-size="large" aria-label="Follow @miyacorata on GitHub">miyacorata</github-button>
                        <a href="https://twitter.com/miyacorata" class="twitter" target="_blank" rel="noopener"><i class="fab fa-twitter"></i>miyacorata</a>
                        <a href="https://instagram.com/miyacorata" class="instagram" target="_blank" rel="noopener"><i class="fab fa-instagram"></i>miyacorata</a>
                        <a href="https://www.pixiv.net/users/19082571" class="pixiv" target="_blank" rel="noopener">pixiv users/19082571</a>
                    </div>
                    <h3>Skills</h3>
                    <p>HTML5, PHP (contain Laravel), CSS, JavaScript, SPARQL</p>
                    <h3>Favorite Contents</h3>
                    <p>少女☆歌劇 レヴュースタァライト, AssaultLily, and more...</p>
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
    #profile .links > a > .fab, #profile .links > a > .fas {
        margin-right: 5px;
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
    #profile .links > a.instagram {
        background: #fafafa;
        border-color: #fafafa;
        color: #262626;
    }
    #profile .links > a.pixiv {
        background: #0097fa;
        border-color: #0097fa;
        color: #ffffff;
    }

    h3 {
        margin: 35px 0 10px;
    }
</style>
