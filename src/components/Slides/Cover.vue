<template>
    <section :data-background-image="require('../../assets/img/valheim-wallpaper.jpeg')">
        <h2 class="r-fit-text text-white-w-shadow" v-html="translations[lang].title"></h2>
        <h4 class="r-fit-text text-white-w-shadow" v-html="translations[lang].subtitle"></h4>
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
                    title: `Valheim <br>Multiplayer Cheat Tool`,
                    subtitle: `Reversing a Game File`,
                },
                pt: {
                    title: `Valheim <br>Ferramenta de <i>Cheat<i>'s`,
                    subtitle: `<i>Reverse Engeering</i> de um Ficheiro do Jogo`,
                }
            }
        }
    },
}
</script>

<style scoped>

</style>