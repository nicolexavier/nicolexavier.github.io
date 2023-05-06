<template>
  <div id="main-content">
    <section id="introduction">
      <div id="container">
        <div id="content-first">Oi!</div>
        <div id="content-line"></div>
        <div id="content-second">Eu sou a <span>Nicole</span></div>
        <div id="content-third">e sou UX/UI Designer.</div>
      </div>
      <div id="face-image">
        <div id="background"><img src="@/assets/selfie.png" /></div>
      </div>
    </section>

    <section id="uxui-works">
      <span id="header">
        Esses são alguns dos meus trabalhos de
        <span class="orange-underline">UX/UI:</span>
      </span>
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
        E aqui tem alguns dos meus trabalhos
        <span class="orange-underline">apenas de UI:</span>
      </span>
      <div class="item"></div>
    </section>

    <section id="about">
      <span id="header">
        E se você quiser saber um pouco mais
        <span class="orange-underline">sobre mim:</span>
      </span>

      <div id="background-container"></div>

      <div id="character-image">
        <img src="@/assets/character.png" />
      </div>

      <div id="content">
        <p>
          Tenho formação e pós-graduação em psicologia e atualmente venho me
          especializando na área do UX/UI design.
        </p>
        <p>
          O interesse surgiu a partir do desejo de maior liberdade criativa. Ter
          a possibilidade de criar interfaces, trabalhar com elementos visuais
          sendo algo que me traz imensa curiosidade e me leva a constante busca
          por conhecimento, sempre me impulsionando a buscar inovação.
        </p>
        <p>
          Procuro unir este meu lado que preza pelo visual, ao lado o qual
          investi muito estudo e apreço que é a psicologia buscando o bem-estar
          e qualidade de vida do indivíduo e usuário levando a importantes
          características de um bom ux/ui designer.
        </p>
      </div>
    </section>

    <section id="footer">
      <div id="header">
        Se quiser entrar em <span class="orange-underline">contato:</span>
      </div>
      <div id="content">
        <div class="item"><button>Behance</button></div>
        <div class="item"><button>LinkedIn</button></div>
        <div class="item"><button>nicolexavierp@gmail.com</button></div>
        <div class="item"><button>Currículo</button></div>
      </div>
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

$breakpoint-mobile: 400px

#main-content
  height: 100%
  width: 100%

  overflow-y: scroll

#introduction
  height: 100vh
  width: 100%

  display: flex
  flex-direction: column

  @media (min-width: $breakpoint-mobile)
    flex-direction: row
    justify-content: center
    align-items: center
    flex-wrap: wrap

  #container
    display: flex
    flex-direction: column

    width: 100%

    margin-top: 20vh

    @media (min-width: $breakpoint-mobile)
      margin-top: 0

      width: 70%

  #content-first
    margin-left: 22%

    color: $base-color-green

    font-weight: 400
    font-size: 4rem

    @media (min-width: $breakpoint-mobile)
      font-size: 6rem

  #content-line
    width: 50%
    height: 0.25rem

    background-color: $base-color-orange

    @media (min-width: $breakpoint-mobile)
      width: 24vw

  #content-second
    align-self: center

    margin-top: 5%

    color: $base-color-green

    font-weight: 500
    font-size: 2.5rem

    @media (min-width: $breakpoint-mobile)
      align-self: flex-start

      margin-top: 1%
      margin-left: 25%

      font-size: 5rem
      font-weight: 400

    span
      background-color: black
      mix-blend-mode: difference

  #content-third
    align-self: center

    color: $base-color-green

    font-weight: 400
    font-size: 1rem

    @media (min-width: $breakpoint-mobile)
      align-self: flex-start

      margin-top: 1%
      margin-left: 30%

      font-size: 2.5rem

  #face-image
    align-self: center

    display: flex
    justify-content: center

    margin-top: 30%

    // background-color: black

    border-radius: 20rem

    @media (min-width: $breakpoint-mobile)
      margin-top: 0

      width: 30vw
      height: 100%

      position: relative

      justify-content: flex-start

    #background
      display: flex

      width: 60%

      border-bottom-right-radius: 50rem
      border-bottom-left-radius: 50rem

      z-index: -999

      @media (min-width: $breakpoint-mobile)
        height: 80%

        background-color: black

      img
        align-self: flex-end

        border-radius: 30rem

        max-height: 100%
        max-width: 100%

        @media (min-width: $breakpoint-mobile)
          align-self: flex-end

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
  height: 60vh

  padding-bottom: 7vh

  background-color: $base-color-green

  display: flex
  flex-direction: column
  align-items: center

  #header
    margin-top: 10%

    align-self: center

    text-align: center

    color: $base-color-grey
    font-weight: 600
    font-size: 1.4rem

  .item
    margin-top: 2rem

    width: 80%
    height: 80%

    background-color: $base-color-grey

#about
  height: 90vh

  padding-bottom: 7vh

  position: relative

  display: flex
  flex-direction: column
  align-items: center

  #header
    margin-top: 10%

    font-size: 1.4rem
    font-weight: 600
    color: $base-color-green

    align-self: center

    text-align: center

  #background-container
    position: absolute

    height: 85%
    width: 90%

    border-top-right-radius: 10rem
    border-top-left-radius: 10rem

    bottom: 0

    background-color: #B3C3C0

    z-index: -999

  #character-image
    margin-top: 15%

    img
      width: 9rem
      height: 9rem

      object-fit: contain

  #content
    position: relative

    width: 80%
    height: 60%

    margin: 2rem

    border: solid 0.125rem $base-color-orange
    border-left: none

    font-size: 0.875rem
    font-weight: 400
    text-indent: 10px
    text-align: justify
    color: $base-color-green

    p
      padding: 0 1rem 0 1rem

  #content::before
    content: ""
    position: absolute

    left: 0px
    bottom: 0px

    height: 50%
    width: 0.125rem

    background: $base-color-orange

#footer
  height: 20vh
  width: 100%

  background-color: $base-color-green

  display: flex
  flex-direction: column
  align-items: center

  #header
    margin-top: 10%

    font-size: 1.2rem
    font-weight: 600
    color: $base-color-grey

  #content
    margin-top: 1rem

    display: grid
    grid-template-columns: repeat(2, 1fr)
    justify-content: center
    align-items: center

    text-align: center

    .item
      font-size: 0.75rem
      font-weight: 600

      padding: 0.5rem

      button
        color: $base-color-grey

        cursor: pointer

        background: none
        border: none

      button:hover
        background-color: black

.orange-underline
  border-bottom: solid 0.125rem $base-color-orange
</style>
