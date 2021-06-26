<template>
    <section>
        <h2 v-html="translations[lang].title"></h2>
        <ul>
            <li v-for="line in translations[lang].text" v-html="line" :key="line"></li>
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
                title: `Features`,
                text: [
                    `multiply inventory items`,
                    `change item levels`,
                    `change character equiped power`,
                    `reset power cool down`,
                    `infinite life`
                ]
            },
            pt: {
                title: `Funcionalidades`,
                text: [
                    `multiplicar itens do inventário`,
                    `alterar os níveis dos itens do inventário`,
                    `alterar o poder equipado`,
                    `fazer reset ao cooldown do poder`,
                    `vida infinita`
                ]
            }
        }
        }
    },
    }
</script>



