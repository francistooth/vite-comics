<script>
   export default {
      name :'Content',
      data() {
         return {
               dcComics:[
                  {
                     text: "Characters",
                     url: "#",
                  },
                  {
                     text: "Comics",
                     url: "#",
                  },
                  {
                     text: "Movies",
                     url: "#",
                  },
                  {
                     text: "TV",
                     url: "#",
                  },
                  {
                     text: "Games",
                     url: "#",
                  },
                  {
                     text: "Videos",
                     url: "#",
                  },
                  {
                     text: "News",
                     url: "#",
                  }                    
               ],
               shop:[
                  {
                     text: "Shop DC",
                     url: "#",
                  },
                  {
                     text: "Shop DC Collectibles",
                     url: "#",
                  }                  
               ],
               dc:[
                  {
                     text: "Terms Of Use",
                     url: "#",
                  },
                  {
                     text: "Privacy policy (New)",
                     url: "#",
                  },
                  {
                     text: "Ad Choices",
                     url: "#",
                  },
                  {
                     text: "Advertising",
                     url: "#",
                  },
                  {
                     text: "Jobs",
                     url: "#",
                  },
                  {
                     text: "Subscriptions",
                     url: "#",
                  },
                  {
                     text: "Talent Workshops",
                     url: "#",
                  },
                  {
                     text: "CPSC Certificates",
                     url: "#",
                  },
                  {
                     text: "Ratings",
                     url: "#",
                  },
                  {
                     text: "Shop Help",
                     url: "#",
                  },
                  {
                     text: "Contact Us",
                     url: "#",
                  }                    
               ],
               sites:[
                  {
                     text: "DC",
                     url: "#",
                  },
                  {
                     text: "MAD Magazine",
                     url: "#",
                  },
                  {
                     text: "DC Kids",
                     url: "#",
                  },
                  {
                     text: "DC Universe",
                     url: "#",
                  },
                  {
                     text: "DC Power Visa",
                     url: "#",
                  }                   
               ]
         }
      },
   }
</script>


<template>
   <div class="component-container">
      <div class="container">
         <div class="nav-menu">
               <div class="left">
                  <div class="dc-comics">
                     <div class="title">
                           DC COMICS
                     </div>
                     <ul >
                           <li v-for="(link,index) in dcComics" :key="index">
                              <a href="#">{{ link.text }}</a>
                           </li>
                     </ul>
                  </div>
                  <div class="shop">
                     <div class="title">
                           SHOP
                     </div>
                     <ul >
                           <li v-for="(link,index) in shop" :key="index">
                              <a href="#">{{ link.text }}</a>
                           </li>
                     </ul>
                  </div>
               </div>
               <div class="center">
                  <div class="dc">
                     <div class="title">
                           DC
                     </div>
                     <ul >
                           <li v-for="(link,index) in dc" :key="index">
                              <a href="#">{{ link.text }}</a>
                           </li>
                     </ul>
                  </div>
               </div>
               <div class="right">
                  <div class="sites">
                     <div class="title">
                           SITES
                     </div>
                     <ul >
                           <li v-for="(link,index) in sites" :key="index">
                              <a href="#">{{ link.text }}</a>
                           </li>
                     </ul>
                  </div>
               </div>
         </div>
         <div class="dc-logo"></div>
      </div>
   </div>
</template>


<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;


.component-container {
   background-image: url(../assets/img/content-bg.jpg);
}

.container {
   height: 50vh;
   display: flex;
   justify-content: space-between;
}

.nav-menu {
   display: flex;
   margin-top: 5%;
   gap: 2vw;
}

.dc-logo {
   background-image: url(../assets/img/dc-logo-bg.png);
   background-repeat: no-repeat;
   background-position: center;
   width: 50%;
}

.title {
   color: white;
   font-size: 18px;
   font-weight: bold;
   margin-bottom: 10%;
}

.dc-comics {
   margin-bottom: 15%;
}

li {
   list-style: none;

   a {
      text-decoration: none;
      color: #959595;
      font-size: 14px;
      line-height: 150%;
   }
   
}
</style>