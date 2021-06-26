<template>
    <section>
        <h2 v-html="translations[lang].title"></h2>
        <p v-html="translations[lang].description"></p>
        <ul>
            <li class="fragment fade-in-then-semi-out" v-html="translations[lang].li1"></li>
            <li class="fragment fade-in-then-semi-out" v-html="translations[lang].li2"></li>
            <li class="fragment fade-in-then-semi-out" v-html="translations[lang].li3"></li>
        </ul>
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
                title: `Results`,
                description: `This method allowed me to find certain things like:`,
                li1: `power cooldown bytes`,
                li2: `item level`,
                li3: `x,y item position in inventory`
            },
            pt: {
                title: `Resultados`,
                description: `Este método permitiu-me encontrar certas coisas como:`,
                li1: `cooldown dos poderes`,
                li2: `nível dos itens`,
                li3: `coordenadas x,y dos itens no inventário`
            }
        }
        }
    },
    }
</script>



