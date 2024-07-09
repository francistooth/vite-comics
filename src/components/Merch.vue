<script>
    export default {
        name :'Merch',
        data() {
            return {
               images:[
                  {
                     image: "buy-comics-digital-comics.png",
                     text: "DIGITAL COMICS"
                  },
                  {
                     image: 'buy-comics-merchandise.png',
                     text: "DC MERCHANDISE"
                  },
                  {
                     image: "buy-comics-shop-locator.png",
                     text: "SUBSCRIPTION"
                  },
                  {
                     image: "buy-comics-subscriptions.png",
                     text: "COMIC SHOP LOCATOR"
                  },
                  {
                     image: "buy-dc-power-visa.svg",
                     text: "DC POWER VISA"
                  },
                  
               ]
            };

        },
        methods: {
            getImagePath: function(img) {
               return new URL(`../assets/img/${img}` , import.meta.url).href;
            }
        }
    }
</script>

<template>
   <div class="component-container">
      <div class="container" >
         <div class="purchase" v-for="(purchase,index) in images" :key="index">
            <a href="#"><div class="icon"><img :src="getImagePath(purchase.image)" alt=""></div> <div class="text">{{ purchase.text }}</div></a>
         </div>
      </div>
   </div>
</template>


<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

.component-container {
   background-color: $blue; 
}

.container {
   @include center(horizontal);
   height: 20vh;
   color: white;
   justify-content: space-between;
}

.purchase {
   a {
      @include center(horizontal);
      text-decoration: none;
      color: white;
      gap: 5px;
   }

   .icon {
      width: 50px;
      height: 50px;
      img {
      height: 100%;
      }
   }
}
</style>