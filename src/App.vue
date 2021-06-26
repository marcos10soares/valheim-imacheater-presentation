<template>
    <div class="reveal" id="app">
      <div class="langselect">
        <a @click="langSelect('en')">en</a> | 
        <a @click="langSelect('pt')">pt</a>
      </div>
      <div class="slides">
        <!-- intro -->
        <Cover :lang="lang"></Cover>
        <WhatIsValheim :lang="lang"></WhatIsValheim>

        <!-- motivation -->
        <section>
          <SectionCover 
            :lang="lang"
            :en="`Motivation`" 
            :pt="`Motivação`"
          ></SectionCover>
          <PersonalMotivation :lang="lang"></PersonalMotivation>
          <Motivation :lang="lang"></Motivation>
        </section>

        <!-- research -->
        <section>
          <SectionCover 
            :lang="lang"
            :en="`Research`" 
            :pt="`Pesquisa`"
          ></SectionCover>
          <OptionsToEaseTheGrind :lang="lang"></OptionsToEaseTheGrind>
          <OfficialConsoleCheatTool :lang="lang"></OfficialConsoleCheatTool>
          <OfficialConsoleCommands :lang="lang"></OfficialConsoleCommands>
          <UnofficialCheatTool :lang="lang"></UnofficialCheatTool>
          <Research :lang="lang"></Research>
          <EasyGifSlide :lang="lang"></EasyGifSlide>
          <CharacterSaveGameFile :lang="lang"></CharacterSaveGameFile>
          <OmgItsBinaryGifSlide :lang="lang"></OmgItsBinaryGifSlide>
        </section>

        <!-- reversing -->
        <section>
          <SectionCover 
            :lang="lang"
            :en="`Reversing<br>the Character File`" 
            :pt="`<i>Reverse Engineering</i><br>o Ficheiro do Personagem`"
          ></SectionCover>
          <ReversingLoadingFile :lang="lang"></ReversingLoadingFile>
          <SubSectionCover 
            :lang="lang"
            :en="`Understanding the File`" 
            :pt="`Interpretar o Ficheiro`"
          ></SubSectionCover>
          <SimpleTitleDescriptionSlide
            :lang="lang"
            :title_en="`Trial and Error`" 
            :desc_en="`The first approach was to directly modify the file, by changing items names and to check the result. This led to a number of bugs.`"
            :title_pt="`Tentativa e Error`"
            :desc_pt="`A primeira abordagem foi tentar modificar o ficheiro directamente, alterando os nomes dos itens e verificando o resultado. Isto levou a inúmeros bugs.`"
          ></SimpleTitleDescriptionSlide>
          <section>
            <h2>{{lang == 'en' ? 'Corrupted Game File' : 'Ficheiro Corrompido'}}</h2>
            <img :src="require('./assets/img/valheim-corrupted-game-file.gif')" alt="">
          </section>
          <section>
            <h2>{{lang == 'en' ? 'Overflows' : 'Overflows'}}</h2>
            <img :src="require('./assets/img/valheim-camera-glitch.gif')" alt="">
          </section>
          <SimpleTitleDescriptionSlide
            :lang="lang"
            :title_en="`Better Approach - DIFF`" 
            :desc_en="`The easiest way to see the differences between the files is just to do a diff, HexFiend supports this feature, and on Windows I used <a href='https://www.cjmweb.net/vbindiff/' target='_blank'>VBinDiff</a> which is a great tool btw.`"
            :title_pt="`Melhor Abordagem - DIFF`"
            :desc_pt="`Uma forma mais fácil de ver as diferenças entre ficheiros é utilizar uma ferramenta de DIFF, o HexFiend tem esta funcionalidade, mas no windows utilizei o <a href='https://www.cjmweb.net/vbindiff/' target='_blank'>VBinDiff</a>.`"
          ></SimpleTitleDescriptionSlide>
          <section>
            <img :src="require('./assets/img/valheim-first-byte.jpeg')" alt="">
          </section>
          <ReversingVBinResults :lang="lang"></ReversingVBinResults>
          <section>
            <img :src="require('./assets/img/vbindiff.gif')" alt="">
          </section>
          <ReversingCodeResult :lang="lang"></ReversingCodeResult>   
          <ReversingFileRegionDiscovery :lang="lang"></ReversingFileRegionDiscovery> 
        </section>

        <!-- the cheat app -->
        <section>
          <SectionCover 
            :lang="lang"
            :en="`Developing<br>The App`" 
            :pt="`Desenvolver<br>a Aplicação`"
          ></SectionCover>
          <GolangApp :lang="lang"></GolangApp> 
          <GolangAppFeatures :lang="lang"></GolangAppFeatures> 

          <!-- image of the app  -->
          <section>
            <img :src="require('./assets/img/gifs/demo_v1.3.0.gif')" alt="">
          </section>

          <!-- challenges -->
          <SimpleTitleDescriptionSlide
            :lang="lang"
            :title_en="`Challenges`" 
            :desc_en="`The biggest challenge of this project still relies on not fully understanding the character file, which leads to a 'finicky' file parsing and some exceptions.`"
            :title_pt="`Desafios`"
            :desc_pt="`De uma forma geral o maior desafio do desenvolvimento desta aplicação ainda é a falta de entendimento do ficheiro da personagem, o que leva a um <i>parsing</i> 'improvisado' e pouco rubusto.`"
          ></SimpleTitleDescriptionSlide>
        </section>
        
        <!-- conclusions -->
        <section>
          <SectionCover 
            :lang="lang"
            :en="`In Conclusion`" 
            :pt="`Conclusões`"
          ></SectionCover>
          <SimpleTitleDescriptionSlide
            :lang="lang"
            :title_en="`Conclusions`" 
            :desc_en="`Ideally would reverse the game binary to fully understand the game file, would result in better file parsing and support for more features.`"
            :title_pt="`Conclusões`"
            :desc_pt="`Idealmente faria-se <i>reverse engineering</i> do binário do jogo para entender completamente o <i>load</i> do ficheiro da personagem, resultaria numa melhor análise do ficheiro e suporte para mais funcionalidades.`"
          ></SimpleTitleDescriptionSlide>
          <SimpleTitleDescriptionSlide
            :lang="lang"
            :title_en="`Conclusions`" 
            :desc_en="`A simple checksum on the game file would prevent most of this project.`"
            :title_pt="`Conclusões`"
            :desc_pt="`Um simples <i>checksum</i> poderia prevenir a maioria deste projecto.`"
          ></SimpleTitleDescriptionSlide>
        </section>

        <!-- the end -->
        <section>
          <h2>Video</h2>
          <iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/LLhJQRQLTpc?autoplay=1&controls=0&showinfo=0&autohide=1&rel=0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </section>
        <UsefulLinks :lang="lang"></UsefulLinks>
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

import ReversingLoadingFile from '@/components/Slides/ReversingLoadingFile'
import ReversingVBinResults from '@/components/Slides/ReversingVBinResults'
import ReversingCodeResult from '@/components/Slides/ReversingCodeResult'
import ReversingFileRegionDiscovery from '@/components/Slides/ReversingFileRegionDiscovery'

import GolangApp from '@/components/Slides/GolangApp'
import GolangAppFeatures from '@/components/Slides/GolangAppFeatures'

import UsefulLinks from '@/components/Slides/UsefulLinks'

import SectionCover from '@/components/SectionCover'
import SubSectionCover from '@/components/SubSectionCover'
import SimpleTitleDescriptionSlide from '@/components/SimpleTitleDescriptionSlide'


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

    ReversingLoadingFile,
    ReversingVBinResults,
    ReversingCodeResult,
    ReversingFileRegionDiscovery,

    GolangApp,
    GolangAppFeatures,

    UsefulLinks,

    SectionCover,
    SubSectionCover,
    SimpleTitleDescriptionSlide,
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
