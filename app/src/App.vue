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

  height: 3rem
  width: 100%

  background-color: #024A59

#logo-container
  display: flex
  flex-direction: row
  justify-content: center
  align-items: center

  margin-left: 5rem

  height: 90%

  color: $nav-font-color
  font-weight: 700
  font-size: 1.5rem

  img
    height: 90%

    object-fit: cover

#links
  display: flex
  flex-direction: row
  justify-content: space-between
  align-items: center

  width: 20%

  margin-right: 5rem

  a
    padding: 0.5rem
    padding-right: 1rem
    padding-left: 1rem

    border-radius: 1rem

    color: $nav-font-color

    font-size: 1.3rem
    text-decoration: none

  a:hover
    background-color: black

    -webkit-transition: all 0.75s ease-in
    -moz-transition: all 0.75s ease-in
    -o-transition: all 0.75s ease-in
    -ms-transition: all 0.75s ease-in
    transition: all 0.75s ease-in
</style>
