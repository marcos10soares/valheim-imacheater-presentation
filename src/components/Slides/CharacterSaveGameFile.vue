<template>
    <section>
        <h2 v-html="translations[lang].title"></h2>

          <!-- eslint-disable -->
          <pre><code data-trim data-noescape>
            C�            P   �     �٠������B�I��BD$��vV�MŦBF��������B獳��B�I��BD$��c@                                                                  
                                                                                                                                                                
                                                                                                                                                                
                                                                                            
            Bjørnm��������!�����H��B���A�/�B�"�FGP_Bonemass����g������SurtlingCore
            ������B�����������������������	ArrowFired������B���������������w�o����Igvar
            PickaxeBronze�����bC���������������m������BjørnShieldBronzeBuckler���LCC����������������m������Bjørn	AxeBronze������C���������������m������Bjørn
            CookedMeat������B�����������������������
            FishCooked������B�����������������������BowHuntsman������B��������������m������BjørnHammer������B���������������m������Bjørn
            CapeTrollHide���L��C��������������m������Bjørn
            ArrowFlintd������B���������������w�o����Igvar
            ArrowFlintd������B���������������w�o����IgvarArrowBronzed������B��������������#�1�����Mike LitorisArmorBronzeChest����ȹD�������������m������BjørnArmorBronzeLegs���s߀D��������������m������Bjørn
            Cloudberry-������B�����������������������BeltStrength������B�����������������������
            CookedLoxMeat������B�����������������������NeckTailGrilled
            ������B�����������������������HelmetTrollLeather���V�JD��������������m������Bjørn	ArrowFired������B��������������d����
          </code></pre>
          <!-- eslint-enable -->
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
          title: `Character File`,
        },
        pt: {
          title: `Ficheiro da Personagem`,
        }
      }
    }
  },
}
</script>