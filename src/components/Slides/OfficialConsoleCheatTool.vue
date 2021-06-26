<template>
    <section>
        <h2 v-html="translations[lang].title"></h2>
          <p v-html="translations[lang].text"></p>

        <div>
          <img class="r-stretch" :src="require('../../assets/img/console.jpeg')" alt="">
        </div>
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
          title: `Valheim Official Console Cheating Tool`,
          text: `This native development console can be both used in singleplayer or multiplayer but just if the server admin allows it.`,
        },
        pt: {
          title: `Ferramenta Oficial de Cheats do Valheim`,
          text: `Esta consola de desenvolvimento pode ser utilizada em singleplayer e em multiplayer (clicando 'F5'), mas apenas se o admin do servidor permitir.`,
        }
      }
    }
  },
}
</script>