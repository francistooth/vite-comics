<script>
   export default {
      name :'SingleCard',
      props: {
         details: Object
      }
   }
</script>




<template>
   <div class="card">
      <img :src="details.thumb" alt="">
      <h3>{{ details.series }}</h3>
   </div>
</template>





<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

.card {
   width: calc(100% / 6 - 20px);
   
   h3 {
      color: $primary;
      font-size: 15px;
      color: #CAD5C4;
      text-align: left;
      padding: 8% 0 16%;
   }

   img {
      display: block;
      height: 170px;
      margin: 0 auto;
      width: 100%;
   }
}
</style>