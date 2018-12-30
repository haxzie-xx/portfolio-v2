<template>
  <div id="app">
    <NavBar title="Haxzie"/>
    <ProfileSection/>
  </div>
</template>

<script>
import NavBar from './components/NavBar.vue'
import ProfileSection from './components/ProfileSection'
import VerticalBar from './components/VerticalBar'

export default {
  name: 'app',
  components: {
    NavBar,
    ProfileSection,
    VerticalBar
  }
}
</script>

<style>
#app {
  font-family: 'Crete Round', serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 90%;
  margin: auto;
  line-height: 1.5em;
  color: #2c3e50;
}
</style>
