<script>
   export default {
      name :'AppContent',
   }
</script>

<template>
   <div class="main">
      <div class="container">
         --> Content goes here <--
      </div>
   </div>
</template>


<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

.main {
   background-color: black; 
}
.container {
   @include center(horizontal);
   height: 20vh;
   color: white;
   font-weight: bold;
   font-size: 24px;
}
</style>