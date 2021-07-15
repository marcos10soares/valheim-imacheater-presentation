<template>
    <section>
        <h2 class="r-fit-text" v-html="translations[lang].title"></h2>
        <ul>
            <li class="fragment fade-in-then-semi-out" v-html="translations[lang].li1"></li>
            <li class="fragment fade-in-then-semi-out" v-html="translations[lang].li2"></li>
            <li class="fragment fade-in-then-semi-out" v-html="translations[lang].li3"></li>
        </ul>
        <p class="fragment r-fit-text" v-html="translations[lang].text"></p>
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
                title: `Main motivation`,
                li1: `Free Game(no risk)`,
                li2: `Dedicated Server`,
                li3: `"CTF like" challenge`,
                li4: `An excuse to try Golang + Lorca/Webview`,
                text: `🤔 can I exploit this? 🤔` 
            },
            pt: {
                title: `Motivação`,
                li1: `Jogo Oferecido (sem risco)`,
                li2: `Servidor Dedicado`,
                li3: `Persistência de dados`,
                text: `🤔 dá para fazer exploit? 🤔`
            }
        }
        }
    },
}
</script>

<style scoped>

</style>

