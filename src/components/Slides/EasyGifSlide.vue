<template>
    <section :data-background-image="require('../../assets/img/gifs/easy.gif')" >
        <h1 style="color: white" v-html="translations[lang].title"></h1>
        <p style="color: white" v-html="translations[lang].subtitle"></p>

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
                title: `Easy`,
                subtitle: `pffff!`,
            },
            pt: {
                title: "Fácil",
                subtitle: `pfff!`,
            }
        }
        }
    },
}
</script>

<style scoped>
</style>