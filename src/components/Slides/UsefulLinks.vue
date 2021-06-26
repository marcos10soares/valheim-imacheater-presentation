<template>
    <section>
        <h2 v-html="translations[lang].title"></h2>
        <ul>
            <li v-for="link in translations[lang].links" :key="link.name">
                <a :href="link.url" target="_blank">{{link.name}}</a>
            </li>
        </ul>
        <div style="margin-top:20px;">
            <img :src="require('../../assets/img/gifs/thankyou.gif')" alt="">
        </div>
        <p>@marcos10soares - instagram - twitter</p>
    </section>
</template>

<script>
export default {
    props: {
        lang: String,
    },
    data() {
        return {
        translations: {
            en: {
                title: `Useful Links`,
                links: [
                    {
                        name: `Blog post about the project`,
                        url: `https://marcossoares.pt/project/2021-03-13-valheim-reversing-game-file`,
                    },
                    {
                        name: `Github Project`,
                        url: `https://github.com/marcos10soares/valheim-imacheater`,
                    },
                    {
                        name: `Youtube Video`,
                        url: `https://www.youtube.com/watch?v=LLhJQRQLTpc`,
                    },
                    {
                        name: `My Personal Website`,
                        url: `https://marcossoares.pt/`,
                    },
                ]
            },
            pt: {
                title: `Links Úteis`,
                links: [
                    {
                        name: `Artigo sobre o projecto`,
                        url: `https://marcossoares.pt/project/2021-03-13-valheim-reversing-game-file`,
                    },
                    {
                        name: `Projecto no Github`,
                        url: `https://github.com/marcos10soares/valheim-imacheater`,
                    },
                    {
                        name: `Video no Youtube`,
                        url: `https://www.youtube.com/watch?v=LLhJQRQLTpc`,
                    },
                    {
                        name: `O meu Website Pessoal`,
                        url: `https://marcossoares.pt/`,
                    },
                ]
            }
        }
        }
    },
    }
</script>



