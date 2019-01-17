<template>
  <div id="app">
    <NavBar title="Haxzie"/>
    <ProfileSection/>
    <Projects/>
    <Experience/>
  </div>
</template>

<script>
import NavBar from './components/NavBar.vue'
import ProfileSection from './components/ProfileSection'
import Projects from './components/Projects'
import Experience from './components/Experience'

export default {
  name: 'app',
  components: {
    NavBar,
    ProfileSection,
    Projects,
    Experience
  }
}
</script>

<style>
html, body {
  min-height: 100%;
  font-size: 16px;
}
#app {
  font-family: 'Crete Round', serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 90%;
  max-width: 1200px;
  margin: auto;
  line-height: 1.5em;
  color: #2c3e50;
}
</style>
