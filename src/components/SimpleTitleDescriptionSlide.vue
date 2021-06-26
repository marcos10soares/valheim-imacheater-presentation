<template>
    <section>
        <h2 v-html="translations[lang].title"></h2>
        <p v-html="translations[lang].description"></p>
    </section>
</template>

<script>
export default {
    props: {
        lang: String,
        title_en: String,
        title_pt: String,
        desc_en: String,
        desc_pt: String,
    },
    data() {
        return {
            translations: {
                en: {
                    title: this.title_en,
                    description: this.desc_en,
                },
                pt: {
                    title: this.title_pt,
                    description: this.desc_pt,
                }
            }
        }
    },
}
</script>

