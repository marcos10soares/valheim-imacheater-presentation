<template>
    <section>
        <h2 v-html="translations[lang].title"></h2>
          <p v-html="translations[lang].text"></p>

          <!-- eslint-disable -->
          <pre><code data-trim data-noescape>
<-- prev |A|  |<---     B     --->||<---                     C                    --->|   |<-- D  -->|
               B  J  ø  ø     R  N
00 00 00 06    42 6A C3 B8    72 6E 6D 1E    F7 D1 00 00    00 00 00 01    1F 20 00 00    18 00 00 00


|<-- E  -->|  |<-- F  -->|    |<-- G  -->|  |<-- H  -->|   |I|| J||<---             K            --->|
                                                                   G  P     _  E  i  k     t  h  y  r
05 03 05 43    05 03 05 43    C3 C3 0C 43    00 63 64 82    45 0A 47 50    5F 45 69 6B    74 68 79 72


|<-- L  -->|  |<--  M  -->|  |<-- N  -->|   |O||<---            P          --->||<---   Q  --->||<-- R 
                                                I  r  o     n  N  a  i     l  s 
00 00 00 00    67 00 00 00    1F 00 00 00    09 49 72 6F    6E 4E 61 69    6C 73 0A 00    00 00 00 00


 -->||<--   X   -->||<--    Y   -->||S||T|  |<---                       U                     --->|| next item -->
C8 42 02 00    00 00 03 00    00 00 00 01    00 00 00 00    00 00 00 6D    1E F7 D1 00    00 00 00 xx
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
          title: `Inventory Region`,
        },
        pt: {
          title: `Região do Inventário`,
        }
      }
    }
  },
}
</script>