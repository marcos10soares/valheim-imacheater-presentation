<template>
  <div class="reveal" id="app">
    <div class="slides">
      <section>{{ message }}</section>
      <section 
        data-background-video="https://static.slid.es/site/homepage/v1/homepage-video-editor.mp4" 
        data-background-video-loop data-background-video-muted>Slide 2</section>
      <section 
        :data-background-image="require('./assets/iconfinder_811462_mark_question_information_sign_icon_128px.png')" 
        data-background-size="100px" 
        data-background-repeat="repeat"
        >
          <h1>Hello World</h1>
          <p class="fragment">Fade in</p>
          <p class="fragment fade-out">Fade out</p>
          <p class="fragment highlight-red">Highlight red</p>
          <p class="fragment fade-in-then-out">Fade in, then out</p>
          <p class="fragment fade-up">Slide up while fading in</p>
      </section>
      <Slide1 ></Slide1>
      <Slide2 ></Slide2>
    </div>

  </div>
</template>

<script>
import Reveal from 'reveal.js/js/reveal'
import Slide1 from '@/components/Slide1'
import Slide2 from '@/components/Slide2'

export default {
  name: 'App',
  components: {
    Slide1,
    Slide2
  },
  data() {
    return {
      message: 'Hello Vue!'
    }
  },
  mounted() {
    Reveal.initialize()
  },
}
</script>

<style>
@import url('../node_modules/reveal.js/css/reveal.css');
@import url('../node_modules/reveal.js/css/theme/white.css');
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
</style>
