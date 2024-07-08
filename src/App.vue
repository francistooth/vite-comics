<script >
import Navbar from './components/Navbar.vue'
import Main from './components/Main.vue'

export default {
  name: 'App',
  components: {
      Navbar,
      Main
  }
}
</script>

<template>
  <Navbar />
  <Main />
</template>

<style lang="scss">
@use './styles/partials/variables' as *;
@use './styles/general.scss' as *;

h1,
h2,
h3,
h4,
h5,
h6 {
  color: $primary;
}
</style>