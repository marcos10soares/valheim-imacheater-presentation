<template>
    <div class="reveal" id="app">
      <div class="langselect">
        <a @click="langSelect('en')">en</a> | 
        <a @click="langSelect('pt')">pt</a>
      </div>
      <div class="slides">
        <Cover :lang="lang"></Cover>
        <WhatIsValheim :lang="lang"></WhatIsValheim>
        <PersonalMotivation :lang="lang"></PersonalMotivation>
        <Motivation :lang="lang"></Motivation>
        <OptionsToEaseTheGrind :lang="lang"></OptionsToEaseTheGrind>
        <section>
          <OfficialConsoleCheatTool :lang="lang"></OfficialConsoleCheatTool>
          <OfficialConsoleCommands :lang="lang"></OfficialConsoleCommands>
        </section>
        <UnofficialCheatTool :lang="lang"></UnofficialCheatTool>
        <Research :lang="lang"></Research>
        <EasyGifSlide :lang="lang"></EasyGifSlide>
        <CharacterSaveGameFile :lang="lang"></CharacterSaveGameFile>
        <OmgItsBinaryGifSlide :lang="lang"></OmgItsBinaryGifSlide>
      </div>
    </div>
</template>

<script>
import Reveal from 'reveal.js/js/reveal'
import Cover from '@/components/Slides/Cover'
import WhatIsValheim from '@/components/Slides/WhatIsValheim'
import PersonalMotivation from '@/components/Slides/PersonalMotivation'
import Motivation from '@/components/Slides/Motivation'
import OptionsToEaseTheGrind from '@/components/Slides/OptionsToEaseTheGrind'
import OfficialConsoleCheatTool from '@/components/Slides/OfficialConsoleCheatTool'
import OfficialConsoleCommands from '@/components/Slides/OfficialConsoleCommands'
import UnofficialCheatTool from '@/components/Slides/UnofficialCheatTool'
import Research from '@/components/Slides/Research'

import EasyGifSlide from '@/components/Slides/EasyGifSlide'
import CharacterSaveGameFile from '@/components/Slides/CharacterSaveGameFile'
import OmgItsBinaryGifSlide from '@/components/Slides/OmgItsBinaryGifSlide'

export default {
  name: 'App',
  components: {
    Cover,
    WhatIsValheim,
    PersonalMotivation,
    Motivation,
    OfficialConsoleCheatTool,
    OptionsToEaseTheGrind,
    OfficialConsoleCommands,
    UnofficialCheatTool,
    Research,
    CharacterSaveGameFile,
    EasyGifSlide,
    OmgItsBinaryGifSlide,
  },
  data() {
    return {
      lang: 'en'
    }
  },
  mounted() {
    Reveal.initialize()
  },
  methods: {
    langSelect(language){
      this.lang = language
    }
  },
}
</script>

<style>
@import url('../node_modules/reveal.js/css/reveal.css');
@import url('../node_modules/reveal.js/css/theme/white.css');
@import './assets/css/main.css';
</style>
