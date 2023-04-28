<template>
  <div id="main-content">
    <div id="introduction">
      <div id="introduction-container">
        <div id="introduction-content-first">Oi!</div>
        <div id="introduction-content-line"></div>
        <div id="introduction-content-second">Eu sou a Nicole</div>
        <div id="introduction-content-third">e sou UX/UI Designer.</div>
      </div>

      <div id="introduction-image"></div>
    </div>
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

#main-content
  height: 100%
  width: 100%

  position: relative

#introduction
  height: 100%
  width: 100%

#introduction-container
  position: absolute

  width: 100%

  top: 30%

  line-height: 0

#introduction-content-first
  margin-left: 12%

  color: $base-color-green

  line-height: 0
  font-weight: 400
  font-size: calc(3vh + 3vw)

#introduction-content-line
  width: 20%
  height: 0.3vh

  margin-top: 3%

  background-color: $base-color-orange

#introduction-content-second
  color: $base-color-green

  margin-top: 3%
  margin-left: 10%

  line-height: 0
  font-weight: 400
  font-size: calc(3vh + 3vw)

#introduction-content-third
  color: $base-color-green

  margin-left: 18%
  margin-top: 4%

  line-height: 0
  font-weight: 400
  font-size: calc(1vh + 1vw)

#introduction-image
  position: absolute

  height: 70%
  width: 15%

  top: 5%
  left: 70%

  background-color: black

  border-bottom-left-radius: 15rem
  border-bottom-right-radius: 15rem
</style>
