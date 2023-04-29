<template>
  <div id="main-content">
    <section id="introduction">
      <div id="container">
        <div id="content-first">Oi!</div>
        <div id="content-line"></div>
        <div id="content-second">Eu sou a Nicole</div>
        <div id="content-third">e sou UX/UI Designer.</div>
      </div>
      <div id="face-image"></div>
    </section>

    <section id="uxui-works">
      <span id="header"> Esses são alguns dos meus trabalhos de UX/UI: </span>
      <div class="item">
        <div class="item-text-content">
          <span>Nara Rubens</span>
          <span>Curso de Micropigmentação</span>
        </div>
        <div class="item-image"></div>
      </div>
      <div class="item">
        <div class="item-text-content">
          <span>Artig</span>
          <span
            >Plataforma de compartilhamento e venda de peças de arte
            autorais.</span
          >
        </div>
        <div class="item-image"></div>
      </div>
    </section>

    <section id="ui-works">
      <span id="header">
        E aqui tem alguns dos meus trabalhos apenas de UI:
      </span>
      <div id="item"></div>
    </section>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "Home",
});
</script>

<style lang="sass">
$base-color-green: #024A59
$base-color-orange: #BF5B05
$base-color-grey: #CCCCCC

#main-content
  height: 100%
  width: 100%

  overflow-y: scroll

#introduction
  height: 100vh
  width: 100%

  display: flex
  flex-direction: column

  #container
    display: flex
    flex-direction: column

    width: 100%

    margin-top: 20vh

  #content-first
    margin-left: 12%

    color: $base-color-green

    font-weight: 400
    font-size: 4rem

  #content-line
    width: 40%
    height: 0.25rem

    background-color: $base-color-orange

  #content-second
    align-self: center

    margin-top: 5%

    color: $base-color-green

    font-weight: 500
    font-size: 2.5rem

  #content-third
    align-self: center

    color: $base-color-green

    font-weight: 400
    font-size: 1rem

  #face-image
    align-self: center

    height: 15rem
    width: 15rem

    margin-top: 20%

    background-color: black

    border-radius: 10rem

#uxui-works
  height: 50vh

  display: flex
  flex-direction: column

  #header
    align-self: center

    text-align: center

    color: $base-color-green
    font-weight: 600
    font-size: 1.5rem

  .item
    width: 75%

    margin-top: 10%

    padding: 1rem

    display: grid
    grid-template-columns: repeat(2, 1fr)
    justify-items: center
    align-items: center

    background-color: $base-color-orange

    border-top-right-radius: 5rem
    border-bottom-right-radius: 5rem

    transition: all 0.5s ease-in-out

  .item:hover
    width: 85%

  .item-text-content
    display: flex
    flex-direction: column
    justify-content: center
    align-items: center
    flex-wrap: wrap
    gap: 0.5rem

    text-align: center
    color: $base-color-grey
    font-size: 0.75rem
    font-weight: 500

    :first-child
      font-size: 1rem
      font-weight: bold

  .item-image
    height: 5rem
    width: 5rem

    border-radius: 3rem

    background-color: black

#ui-works
  height: 50vh

  background-color: $base-color-green

  display: flex
  flex-direction: column

  #header
    margin-top: 10%

    align-self: center

    text-align: center

    color: $base-color-grey
    font-weight: 600
    font-size: 1.4rem
</style>
