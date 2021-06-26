<template>
    <section 
        data-background-iframe="https://www.youtube.com/embed/JeF79O32s9o?autoplay=1&controls=0&showinfo=0&autohide=1&rel=0"
    >
        <h2 class="text-white-w-shadow" v-html="translations[lang].title"></h2>
        <ul>
            <li class="text-white-w-shadow" v-html="translations[lang].li1"></li>
            <li class="text-white-w-shadow" v-html="translations[lang].li2"></li>
        </ul>
        <p class="fragment text-white-w-shadow" v-html="translations[lang].text"></p>
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
                title: `What is Valheim`,
                li1: `survival and sandbox game`,
                li2: `focused on building, crafting and exploration`,
                text: `Great Game! ❤️ but... <b>too much grind for me! 😅</b>`,
            },
            pt: {
                title: "O Que é o Valheim",
                li1: `um jogo 'sandbox' e de sobrevivência`,
                li2: `focado em construção, 'crafting' e exploração`,
                text: `Excelente jogo! ❤️ mas... <b>tem demasiado 'grind' para mim! 😅</b>`,
            }
        }
        }
    },
}
</script>