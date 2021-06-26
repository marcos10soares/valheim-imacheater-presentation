<template>
    <section>
        <h2 class="r-fit-text" v-html="translations[lang].title"></h2>
        <p class="r-fit-text" v-html="translations[lang].text1"></p>
        <p class="r-fit-text" v-html="translations[lang].text2"></p>
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
                    title: `Personal Motivation`,
                    text1: `A friend of mine offered me this game when it launched, and we played on our dedicated server for some days.`,
                    text2: `I then realized <b>the game character would keep the items between multiplayer servers</b>, also <b>stats like life and stamina did not change when moving from server to server</b>, or even from local to server... <br> 🤔 can we exploit that?`
                },
                pt: {
                    title: `Motivação Pessoal`,
                    text1: `Um amigo ofereceu-me este jogo quando foi lançado, e jogámos no nosso servidor dedicado durante alguns dias.`,
                    text2: `Percebi então <b>que o personagem mantinha os itens do inventário entre servidores multiplayer</b>, assim como <b>stats como a vida e a stamina não mudavam de servidor para servidor</b>, ou mesmo de local para online... <br>🤔 dá para fazer exploit?`
                }
            }
        }
    },
}
</script>

<style scoped>

</style>

