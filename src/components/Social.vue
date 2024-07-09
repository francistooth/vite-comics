<script>
export default {
   name :'Social',
   data() {
      return {
         socials:[
            {
               name: "facebook",
               icon: "footer-facebook.png",
               url: "#",
            },
            {
               name: "twitter",
               icon: "footer-twitter.png",
               url: "#",
            },
            {
               name: "youtube",
               icon: "footer-youtube.png",
               url: "#",
            },
            {
               name: "pinterest",
               icon: "footer-pinterest.png",
               url: "#",
            },
            {
               name: "find-us",
               icon: "footer-periscope.png",
               url: "#",
            },                  
         ],
      }
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
         <div class="sign-up">
               <a href="#">SIGN-UP NOW!</a>
         </div>
         <div class="social-icons">
               <div class="follow">
                  <a href="#">FOLLOW US</a>
               </div>
               <div class="icons-container" >
                  <div :class="social.name" v-for="(social,index) in socials" :key="index">
                     <a :href="social.url">
                        <img :src="getImagePath(social.icon)" alt="">
                     </a>
                  </div>
               </div>
         </div>
      </div>
   </div>
</template>


<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;


.component-container {
   background-color: #303030;
   height: $nav;
}

.container {
   display: flex;
   height: 100%;
   justify-content: space-between
}

.sign-up {
   @include center(horizontal);
   
   a {
      color: white ;
      font-weight: bold;
      font-size: 18px;
      text-decoration: none;
      border: 3px solid $blue;
      padding: 10px
   }
}

.social-icons {
   @include center(horizontal);
   width: 31%;
}

.follow  {
   width: 30%;
   a {
      color: $blue;
      font-weight: bold;
      font-size: 18px;
      text-decoration: none;
   }
}

.icons-container {
   display: flex;
   gap: 6%;
   width: 70%;
   transform: scale(0.8);
}
</style>