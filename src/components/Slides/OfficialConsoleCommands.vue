<template>
    <section>
        <h2 v-html="translations[lang].title"></h2>
          <p v-html="translations[lang].text"></p>

          <pre><code data-trim data-noescape>
            god - Enables god mode.
            ghost - Enables Ghost Mode. Enemies will ignore you.
            heal - Heals your character to full health.
            puke - Resets your character's hunger, while also restoring default health and stamina.
            pos – Print current player position.
            hair - permanently removes your hair.
            beard - permanently removes your beard.
            model [0/1] - Changes your character model between masculine and feminine body types.
            resetcharacter – Reset Character data.
            raiseskill [skill] [amount] – Raise skill level (for example raiseskill jump 100).
            resetskill [skill name] - Resets skill level to 0.
            goto [x,z] Teleports player to the specified coordinates.
            spawn [item_name] [item_quantity] - spawns an item in with a quantity.
          </code></pre>

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
          title: `Official Commands`,
          text: `Some of the commands:`,
        },
        pt: {
          title: `Comandos Oficiais`,
          text: `Alguns dos comandos:`,
        }
      }
    }
  },
}
</script>