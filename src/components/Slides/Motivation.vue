<template>
    <section>
        <h2 v-html="translations[lang].title"></h2>
        <ul>
          <li class="fragment fade-in-then-semi-out" v-html="translations[lang].li1"></li>
          <li class="fragment fade-in-then-semi-out" v-html="translations[lang].li2"></li>
          <li class="fragment fade-in-then-semi-out" v-html="translations[lang].li3"></li>
          <li class="fragment fade-in-then-semi-out" v-html="translations[lang].li4"></li>
          <li class="fragment fade-in-then-semi-out" v-html="translations[lang].li5"></li>
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
          title: `Main motivation`,
          li1: `<b>Ease the grind</b>`,
          li2: `Curiosity & Fun`,
          li3: `"CTF like" challenge`,
          li4: `An excuse to try Golang + Lorca/Webview`,
          li5: `Bonus: Annoy my friends 😃`
        },
        pt: {
          title: `Motivação`,
          li1: `<b>Reduzir o <i>grind</i></b>`,
          li2: `Curiosidade & Diversão`,
          li3: `Desafio estilo "CTF"`,
          li4: `Uma desculpa para usar Golang + Lorca/Webview`,
          li5: `Bonus: Chatear amigos 😃`
        }
      }
    }
  },
}
</script>