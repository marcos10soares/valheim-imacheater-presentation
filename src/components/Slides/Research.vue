<template>
    <section>
        <h2 v-html="translations[lang].title"></h2>
        <p v-html="translations[lang].subtitle"></p>
        <ul>
          <li class="fragment fade-in-then-semi-out" v-html="translations[lang].li1"></li>
          <li class="fragment fade-in-then-semi-out" v-html="translations[lang].li2"></li>
          <li class="fragment fade-in-then-semi-out" v-html="translations[lang].li3"></li>
          <li class="fragment fade-in-then-semi-out" v-html="translations[lang].li4"></li>
        </ul>
        <p class="fragment" v-html="translations[lang].gotcha"></p>
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
          title: `Research`,
          subtitle: `Researched possible options:`,
          li1: `Looking for in-game exploits, as in actions a player could do that would lead to unwanted results by the game developers`,
          li2: `Modifying game files`,
          li3: `Modifying server requests`,
          li4: `Modifying ram values, using cheat engine (some risks associated)`,
          gotcha: `<b>Decided to use the character game file!</b>`,
        },
        pt: {
          title: `Pesquisa`,
          subtitle: `Avaliação de possíves opções:`,
          li1: `Procurar por <i>in-game exploits</i>, no sentido de acções que permitam obter resultados não desejados pelos criadores do jogo`,
          li2: `Modificar ficheiros do jogo`,
          li3: `Modificar pedidos ao servidor`,
          li4: `Modificar valores da ram (utilizando o CheatEngine - alguns riscos)`,
          gotcha: `<b>Decidi utilizar o <i>savegame</i>(ficheiro) da personagem!</b>`,
        }
      }
    }
  },
}
</script>