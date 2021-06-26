<template>
    <section>
        <h2 v-html="translations[lang].title"></h2>
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
          title: `Options to Ease The Grind`,
          li1: `Convince your friends to do all the work 😃`,
          li2: `Cheat in singleplayer, load your inventory with as much items as possible and join a multiplayer server`,
          li3: `Cheat online if your server admin allows you`,
        },
        pt: {
          title: `Formas de Reduzir o <i>Grind</i>`,
          li1: `Convencerem os vossos amigos a apanhar recursos por vocês 😃`,
          li2: `Usar a consola de cheats em singleplayer e levarem o máximo de items no vosso inventário`,
          li3: `Utilizar cheats online se o admin do vosso servidor activar a consola de cheats`,
        }
      }
    }
  },
}
</script>