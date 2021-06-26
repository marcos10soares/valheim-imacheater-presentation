<template>
    <section>
        <h2 v-html="translations[lang].title"></h2>
        <p v-html="translations[lang].description"></p>
        <ul>
          <li v-for="item in translations[lang].list" class="fragment fade-in-then-semi-out" v-html="item" :key="item"></li>
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
          title: `Save Game File`,
          description: `So far the regions I managed to identify:`,
          list: [
            `Header`,
            `Chunks of mostly zeros`,
            `Map Markers Region`,
            `Character Stats and Inventory Region`,
            `Discovered Items and Recipes Region`,
            `Food Items Region`,
          ]

        },
        pt: {
          title: `Ficheiro do Personagem`,
          description: `Até ao momento consegui identificar as seguintes regiões:`,
          list: [
            `Cabeçalho`,
            `Bloco de Zeros`,
            `Marcadores do Mapa`,
            `Inventário e Características do Personagem`,
            `Itens e Receitas já descobertos`,
            `Itens de comida`,
          ]
        }
      }
    }
  },
}
</script>
