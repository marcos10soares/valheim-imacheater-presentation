<template>
    <section>
        <h2 v-html="translations[lang].title"></h2>
        <p v-html="translations[lang].description"></p>
        <div>
            <img style="max-width: 400;" :src="require('../../assets/img/valheim-hex-editor-vscode.jpeg')" alt="">
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
                    title: `Loading the character file`,
                    description: `<p>Since it's a binary file, the next step was to load it on a hex editor. For a quick preview I used <a href="https://marketplace.visualstudio.com/items?itemName=ms-vscode.hexeditor">VS Code plugin "Hex Editor"</a> but then moved to <a href="https://hexfiend.com/">HexFiend</a> (on MacOS) and <a href="https://en.wikipedia.org/wiki/Frhed">Frhed</a> (on Windows).</p>`,
                },
                pt: {
                    title: `Abrir o ficheiro da Personagem`,
                    description: `<p>Como é um ficheiro binário, o próximo passo foi abri-lo num editor de hexadecimal. Para uma pré-visualização rápida, utilizei o plugin do <a href="https://marketplace.visualstudio.com/items?itemName=ms-vscode.hexeditor">VS Code - "Hex Editor"</a> mas depois acabei a usar o <a href="https://hexfiend.com/">HexFiend</a> (em MacOS) e <a href="https://en.wikipedia.org/wiki/Frhed">Frhed</a> (no Windows).</p>`,
                }
            }
        }
    },
}
</script>

<style scoped>

</style>         
