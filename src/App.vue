<script >
import Navbar from './components/Navbar.vue'
// import Main from './components/Main.vue' no content
import CardContainer from './components/CardContainer.vue' // main with content
import Merch from './components/Merch.vue'
import Content from './components/Content.vue'
import Social from './components/Social.vue'

export default {
  name: 'App',
  components: {
      Navbar,
      // Main, no content
      CardContainer,
      Merch,
      Content,
      Social
  }
}
</script>

<template>
   <Navbar />
   <!-- <Main /> no content -->
   <CardContainer />
   <Merch />
   <Content />
   <Social />
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