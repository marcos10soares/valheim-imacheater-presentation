<template>
    <section :data-background-image="require('../../assets/img/gifs/surprise_giphy.gif')" >
        <h1 class="r-fit-text text-white-w-shadow" v-html="translations[lang].title"></h1>
        <p class="r-fit-text text-white-w-shadow" v-html="translations[lang].subtitle"></p>

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
                title: `OMG`,
                subtitle: `It's a binary file! 🤦🏻‍♂️`,
            },
            pt: {
                title: "OMG",
                subtitle: `É um ficheiro binário! 🤦🏻‍♂️`,
            }
        }
        }
    },
}
</script>
<style scoped>
</style>