<template>
    <section>
        <h2 v-html="translations[lang].title"></h2>
        <p v-for="line in translations[lang].text" v-html="line" :key="line"></p>

        <div>
            <img style="border:0px; box-shadow:none;" :src="require('../../assets/img/golorcaapp.png')" alt="">
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
                    title: `Imacheater App`,
                    text: [
                        `This app was done using Golang + Lorca Framework.`,
                        `It uses Chrome browser as a UI layer. Lorca establishes a connection to the browser window and allows calling Go code from the UI and manipulating UI from Go in a seamless manner.`
                    ]
                },
                pt: {
                    title: `Aplicação Imacheater`,
                    text: [
                        `Esta aplicação foi desenvolvida utilizando Golang + a Framework Lorca.`,
                        `Utiliza o navegador Chrome como uma camada de UI. A framework Lorca estabelece uma ligação à janela do navegador e permite ligar o código Go a partir do UI e manipular o UI a partir do Go de uma forma contínua e bidirecional.`,
                    ]
                }
            }
        }
    },
}
</script>