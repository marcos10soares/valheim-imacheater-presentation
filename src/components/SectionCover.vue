<template>
    <section data-background-color="#091b28">
        <h2 class="r-fit-text text-white-w-shadow" v-html="translations[lang].title"></h2>
    </section>
</template>

<script>
export default {
    props: {
        lang: String,
        en: String,
        pt: String
    },
    data() {
        return {
            translations: {
                en: {
                    title: this.en
                },
                pt: {
                    title: this.pt,
                }
            }
        }
    },
}
</script>

<style scoped>

</style>