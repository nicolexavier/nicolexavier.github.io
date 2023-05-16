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
        E aqui tem alguns dos meus trabalhos
        <span class="orange-underline">apenas de UI:</span>
      </span>
      <q-carousel
        v-model="slide"
        swipeable
        animated
        control-type="flat"
        control-color="blue"
        navigation
        padding
        arrows
        class="rounded-borders"
      >
        <q-carousel-slide name="artig" class="column no-wrap flex-center">
          <div class="carousel-item">
            <img src="@/assets/artig-logo.png" id="artig-logo" />
            <span id="header">Artig</span>
            <div class="carousel-item-btns">
              <q-btn outline dense label="UX/UI" style="color: #bf5b05"></q-btn>
              <q-btn
                outline
                dense
                label="Apenas UI"
                style="color: #024a59"
              ></q-btn>
            </div></div
        ></q-carousel-slide>

        <q-carousel-slide name="nara" class="column no-wrap flex-center">
          <div class="carousel-item">
            <img src="@/assets/nara-logo.png" id="nara-logo" />
            <span id="header">Landing Page (Curso)</span>
            <div class="carousel-item-btns">
              <q-btn outline dense label="UX/UI" style="color: #bf5b05"></q-btn>
              <q-btn
                outline
                dense
                label="Apenas UI"
                style="color: #024a59"
              ></q-btn>
            </div></div
        ></q-carousel-slide>
      </q-carousel>
    </section>

    <section id="about">
      <span id="header">
        E se você quiser saber um pouco mais
        <span class="orange-underline">sobre mim:</span>
      </span>

      <div id="content-container">
        <div id="character-image">
          <img src="@/assets/character.png" />
        </div>

        <div id="content">
          <p>
            Tenho formação e pós-graduação em psicologia e atualmente venho me
            especializando na área do UX/UI design.
          </p>
          <p>
            O interesse surgiu a partir do desejo de maior liberdade criativa.
            Ter a possibilidade de criar interfaces, trabalhar com elementos
            visuais sendo algo que me traz imensa curiosidade e me leva a
            constante busca por conhecimento, sempre me impulsionando a buscar
            inovação.
          </p>
          <p>
            Procuro unir este meu lado que preza pelo visual, ao lado o qual
            investi muito estudo e apreço que é a psicologia buscando o
            bem-estar e qualidade de vida do indivíduo e usuário levando a
            importantes características de um bom ux/ui designer.
          </p>
        </div>
      </div>
    </section>

    <section id="footer">
      <div id="header">
        Entre em <span class="orange-underline">contato:</span>
      </div>
      <div id="content">
        <div class="item">
          <button><q-icon name="email" />nicolexavierp@gmail.com</button>
        </div>
        <div class="item">
          <button
            onclick="window.open('https://www.behance.net/nicolexavier2','_blank')"
          >
            <q-icon name="image" />Behance
          </button>
        </div>
        <div class="item">
          <button
            onclick="window.open('https://www.linkedin.com/in/nicole-xavier-97b603262/','_blank')"
          >
            <q-icon name="badge" />LinkedIn
          </button>
        </div>
        <div class="item">
          <button><q-icon name="download" />Currículo</button>
        </div>
      </div>
    </section>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "Home",
  data() {
    return {
      slide: ref("artig"),
    };
  },
});
</script>

<style lang="sass">
$base-color-green: #024A59
$base-color-orange: #BF5B05
$base-color-grey: #ededed

$breakpoint-mobile: 450px

#main-content
  height: 100%
  width: 100%

  overflow-y: scroll

#introduction
  height: 100%
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
      background-image: url("@/assets/color-background-sm.png")
      background-clip: text
      -webkit-background-clip: text
      color: transparent
      font-weight: bold

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
      height: 100%

      border-radius: 55rem

      -webkit-box-shadow: 0px 0px 39px 4px rgba(105,105,105,1)
      -moz-box-shadow: 0px 0px 39px 4px rgba(105,105,105,1)
      box-shadow: 0px 0px 39px 4px rgba(105,105,105,1)

      z-index: 0

      background-image: url("@/assets/color-background-sm.png")

      @media (min-width: $breakpoint-mobile)
        height: 80%

        background-image: url("@/assets/color-background.png")

        border-radius: 0
        border-bottom-right-radius: 50rem
        border-bottom-left-radius: 50rem

        background-color: black

      img
        align-self: flex-end

        max-height: 100%
        max-width: 100%

        border-radius: 30rem

        @media (min-width: $breakpoint-mobile)
          align-self: flex-end

#uxui-works
  height: 70vh

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

    @media (min-width: $breakpoint-mobile)
      margin-top: 2%
      font-size: 2.3rem

  .q-carousel
    margin-top: 2rem
    margin-bottom: 2rem

    height: 100%

    border-radius: 15rem

    .q-carousel__slide
      padding: 0
      padding-top: 1rem
      padding-bottom: 4rem

      width: 17rem

      @media (min-width: $breakpoint-mobile)
        width: 20rem
        padding-top: 1rem
        padding-bottom: 4rem

  .carousel-item
    height: 100%

    display: flex
    flex-direction: column
    justify-content: space-between
    align-items: center

    text-align: center

    #header
      font-size: 1.2rem
      overflow-wrap: break-word

      margin-top: 0

      max-width: 70%

      color: $base-color-green
      border-bottom: solid 0.2rem $base-color-orange

      @media (min-width: $breakpoint-mobile)
        font-size: 1.5rem

    #artig-logo
      width: 8rem

      @media (min-width: $breakpoint-mobile)
        width: 9rem

    #nara-logo
      width: 12rem

      margin-top: 20%

      @media (min-width: $breakpoint-mobile)
        width: 15rem

  .carousel-item-btns
    display: flex
    flex-direction: column
    gap: 0.5rem

    font-weight: bolder!important

    .q-btn
      border-radius: 1rem

    span
      padding-right: 1rem
      padding-left: 1rem

  .q-carousel__navigation-icon i
    font-size: 13px

#about
  height: auto

  display: flex
  flex-direction: column
  align-items: center

  @media (min-width: $breakpoint-mobile)
    height: 60vh

  #header
    margin-top: 10%

    font-size: 1.4rem
    font-weight: 600
    color: $base-color-green

    align-self: center

    text-align: center

    @media (min-width: $breakpoint-mobile)
      margin-top: 3%

      font-size: 2.3rem

  #content-container
    display: flex
    flex-direction: column
    justify-content: center
    align-items: center

    width: 85%

    margin-top: 10%

    border-top-right-radius: 9rem
    border-top-left-radius: 9rem

    background-color: #B3C3C0

    @media (min-width: $breakpoint-mobile)
      margin-top: 3%

      height: 100%

      flex-direction: row

  #character-image
    margin-top: 15%

    @media (min-width: $breakpoint-mobile)
      margin-top: 0

      width: 15%

    img
      width: 9rem

      object-fit: contain

      @media (min-width: $breakpoint-mobile)
        width: 100%

  #content
    position: relative

    width: 85%
    height: 60%

    margin: 9%

    padding: 0.5rem

    border: solid 0.125rem $base-color-orange
    border-left: none

    font-size: clamp(0.8rem, 1vw + 0.5rem, 2rem)
    font-weight: 500
    text-indent: 10px
    text-align: justify
    color: $base-color-green

    @media (min-width: $breakpoint-mobile)
        max-width: 60%

        font-size: clamp(0.5rem, 0.6vw + 0.25rem, 1rem)
        font-weight: 600

        margin: 0
        margin-left: 5%

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
  justify-content: center

  z-index: 100

  #header
    font-size: 1.2rem
    font-weight: 600
    color: $base-color-grey

    @media (min-width: $breakpoint-mobile)
      font-size: 2rem

  #content
    margin-top: 1rem

    display: flex
    flex-direction: row
    flex-wrap: wrap
    justify-content: center
    align-items: center

    text-align: center

    @media (min-width: $breakpoint-mobile)
      margin-top: 2rem

    .item
      padding: 0.5rem

      button
        color: $base-color-grey

        cursor: pointer

        background: none
        border: none
        border-radius: 10px
        border: dashed 1px grey

        font-size: 0.9rem

        -webkit-touch-callout: text
        -webkit-user-select: text
        -khtml-user-select: text
        -moz-user-select: text
        -ms-user-select: text
        user-select: text

        @media (min-width: $breakpoint-mobile)
          font-size: 1.25rem
          font-weight: 400

        .q-icon
          margin-right: 5px

      button:hover
        background-color: rgb(192, 91, 5, 0.8)

.orange-underline
  border-bottom: solid 0.125rem $base-color-orange
</style>
