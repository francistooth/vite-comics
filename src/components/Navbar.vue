<script>
   export default {
      name :'AppNav',
      data() {
         return {
            links:[
               {
                  text: "CHARACTERS",
                  url: "#",
                  status: false,
               },
               {
                  text: "COMICS",
                  url: "#",
                  status: false,
               },
               {
                  text: "MOVIES",
                  url: "#",
                  status: false,
               },
               {
                  text: "TV",
                  url: "#",
                  status: false,
               },
               {
                  text: "GAMES",
                  url: "#",
                  status: false,
               },
               {
                  text: "COLLECTIBLES",
                  url: "#",
                  status: false,
               },
               {
                  text: "VIDEOS",
                  url: "#",
                  status: false,
               },
               {
                  text: "FANS",
                  url: "#",
                  status: false,
               },
               {
                  text: "NEWS",
                  url: "#",
                  status: false,
               },
               {
                  text: "SHOP",
                  url: "#",
                  status: false,
               },
               
            ],
            currentIndex: 0,
         }
         
      },
      methods: {
         toggleNav(index) {
         this.currentIndex = index;
      }
      }
   }
</script>

<template>
   <div class="component-container">
      <div class="container">
      <div class="dc-logo">
         <a href="#">
            <img src="../assets/img/dc-logo.png" alt="">
         </a>
      </div>
      <nav class="dc-nav">
         <ul >
            <li v-for="(link,index) in links" :key="index" @click="toggleNav(index)">
               <a href="#" class="bordo" :class="currentIndex === index ? 'active' : '' ">{{ link.text }}</a>
            </li>
         </ul>
      </nav>
   </div>
   </div>
</template>


<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

.container {
   @include center(horizontal);
   justify-content: space-between;
   height: $nav; 
}

.dc-logo {
   transform: scale(0.7);
}

ul {
   list-style: none;
   display: flex;
   gap: 2%;
   font-size: 12px;
   margin-right: 2%;
}

li a {
   text-decoration: none;
   font-weight: bold;
   height: $nav;
   @include center;

   &.bordo {
      border-bottom: 4px solid transparent;
      &.active,
      &:hover {
         border-bottom-color:$blue;
         color: $blue;
      }
   }  
}

</style>