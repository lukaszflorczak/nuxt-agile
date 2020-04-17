<template>
  <div class="container">
    <logo/>
    <h1 class="title">
      nuxt-agile
    </h1>
    <h2 class="subtitle">
      Demo of VueAgile carousel & Nuxt.js with SSR
    </h2>

    <div class="row">
      <div class="demo demo--1">
        <h3>SSR</h3>
        <carousel/>
      </div>

      <div class="demo demo--2">
        <h3>Client only</h3>
        <client-only placeholder="Carousel loading...">
          <carousel/>
        </client-only>
      </div>
    </div>
  </div>
</template>

<script>
  import Logo from '~/components/Logo.vue'
  import Carousel from '~/components/Carousel.vue'

  export default {
    components: {
      Logo,
      Carousel
    }
  }
</script>

<style>
  .container {
    margin: 0 auto;
    max-width: 900px;
    min-height: 100vh;
    padding: 30px 0;
    text-align: center;
  }

  .title {
    font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
    display: block;
    font-weight: 300;
    font-size: 100px;
    color: #35495e;
    letter-spacing: 1px;
  }

  .subtitle {
    font-weight: 300;
    font-size: 42px;
    color: #526488;
    word-spacing: 5px;
    padding-bottom: 15px;
  }

  .client-only-placeholder {
    align-items: center;
    background-color: #ddd;
    display: flex;
    justify-content: center;
    margin-top: 20px;
    min-height: 200px;
  }

  .row {
    display: flex;
    justify-content: space-between;
  }

  .demo {
    margin-top: 30px;
    width: calc(50% - 10px);
  }

  .demo h3 {
    font-weight: 300;
    font-size: 24px;
    color: #526488;
    word-spacing: 5px;
  }
</style>
