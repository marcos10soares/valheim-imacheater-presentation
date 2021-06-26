<template>
    <section>
        <h2 v-html="translations[lang].title"></h2>
        <p v-html="translations[lang].subtitle"></p>
        <ul>
          <li class="fragment" v-html="translations[lang].li1"></li>
          <li class="fragment" v-html="translations[lang].li2"></li>
          <li class="fragment" v-html="translations[lang].li3"></li>
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
          title: `My Unofficial Cheating Tool`,
          subtitle: `Goals:`,
          li1: `easy to use`,
          li2: `ui interface`,
          li3: `work in multiplayer (independently of admin approval)`,
        },
        pt: {
          title: `A minha Ferramenta Não Oficial`,
          subtitle: `Objectivos:`,
          li1: `fácil utilização`,
          li2: `interface gráfico`,
          li3: `funcionar em multiplayer (independentemente da autorização de admin do servidor)`,
        }
      }
    }
  },
}
</script>
