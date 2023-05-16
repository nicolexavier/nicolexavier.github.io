<template>
  <nav id="navbar">
    <div id="logo-container">
      <img src="@/assets/logo.png" />
      Nicole.
    </div>
    <div id="links">
      <router-link to="/works">Trabalhos</router-link>
      <router-link to="/about">Sobre</router-link>
      <router-link to="/contact">Contato</router-link>
    </div>
  </nav>
  <div id="wrapper">
    <router-view />
  </div>
</template>

<style lang="sass">
$nav-font-color: #CCCCCC
$nav-link-font-hover: #CCCCCC


@font-face
  font-family: 'Montserrat'
  src: url("@/assets/fonts/montserrat/montserrat-variable.ttf")

*
  font-family: 'Montserrat', sans-serif

html, body
  width: 100%
  height: 100%
  margin: 0
  padding: 0

  background-color: #e6e6e6

#app
  width: 100%
  height: 100%

#wrapper
  width: 100%
  height: 100%
  display: flex
  flex-direction: column
  justify-content: center
  align-items: center

#navbar
  position: fixed

  display: flex
  flex-direction: row
  justify-content: space-between
  align-items: center

  height: 5%
  width: 100%

  background-color: #024A59

  font-weight: 700

  z-index: 9999

#logo-container
  display: flex
  flex-direction: row
  justify-content: center
  align-items: center

  margin-left: 5%

  height: 90%

  color: $nav-font-color

  font-size: clamp(1rem, 1vw + 0.5rem, 5rem)

  img
    height: 90%

    object-fit: cover

#links
  display: flex
  flex-direction: row
  justify-content: space-between
  align-items: center

  width: max(12rem, 20%)

  margin-right: 5%

  font-size: clamp(0.5rem, 0.75vw + 0.25rem, 5rem)

  a
    padding: 0.25rem
    padding-right: 1rem
    padding-left: 1rem

    border-radius: 1rem

    color: $nav-font-color

    text-decoration: none

  a:hover
    background-color: rgb(192, 91, 5, 0.8)

    -webkit-transition: all 0.5s ease-out
    -moz-transition: all 0.5s ease-out
    -o-transition: all 0.5s ease-out
    -ms-transition: all 0.5s ease-out
    transition: all 0.5s ease-out
</style>
