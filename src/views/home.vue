<template>
  <v-app>
    <v-container
    fluid
    class="main"
    >
    <v-container class="container-fluid">

    <!-- start of navigation div -->
   <v-card class="">
    <v-app-bar
      absolute
      color="#6A76AB"
      dark
      prominent
      src="https://picsum.photos/1920/1080?random"
    >
      <template v-slot:img="{ props }">
        <v-img
          v-bind="props"
          gradient="to top right, rgba(100,115,201,.7), rgba(25,32,72,.7)"
        ></v-img>
      </template>

      <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-app-bar-title>Title</v-app-bar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>

      <template v-slot:extension>
         <v-div class="navigate mt-4">
        <v-flex class="subnav-content">
        <div class="nav-content">
          <div ><router-link class="navlinks" to="/" style="color:white">Home</router-link></div>
          <div ><router-link class="navlinks" to="products" style="color:white"> Products</router-link></div>
          <div ><router-link class="navlinks" to="services" style="color:white"> Services</router-link></div>
          <div ><router-link class="navlinks" to="about" style="color:white"> About Us</router-link></div>
        </div>
      </v-flex>
    </v-div>

      </template>
    </v-app-bar>
  </v-card>
    <!-- end of page navigation div -->

    <!-- start of header div -->
    <!-- <div class="mask pattern-8 header col-md-12">
      <video autoplay muted loop class="mask pattern-8">
      <source src="../assets/header.mp4"  type="video/mp4">
    </video>
    </div>
     -->
   
    <!-- end of header div -->

    <!-- begin of page intro -->
    <div class="intro black">
      <v-col
          cols="12"
          sm="12"
        >
         <md-card>
      <md-card-media-cover md-solid>
        <md-card-media md-ratio="1:1">
          <img src="/assets/examples/card-sky.jpg" alt="Skyscraper">
        </md-card-media>

        <md-card-area>
          <md-card-header>
            <span class="md-title">Solid background</span>
            <span class="md-subhead">1/1 image</span>
          </md-card-header>

          <md-card-actions>
            <md-button class="md-icon-button">
              <md-icon>favorite</md-icon>
            </md-button>

            <md-button class="md-icon-button">
              <md-icon>share</md-icon>
            </md-button>
          </md-card-actions>
        </md-card-area>
      </md-card-media-cover>
    </md-card>
        </v-col>
    </div>
    <!-- end of page intro -->
  </v-container>
    </v-container>
  </v-app>
</template>

<script>
export default {
  
  }
</script>

<style>
.main{
  background-image: url("../assets/background.png");
  position: fixed;
  height: 100%;
  width: 80vw;
  border-radius: 0px;
  opacity: ;
}
.container-fluid{
  background:	#E8E8E8;
  height: 100vh;
  position: absolute;
  top: 0px;
  left: 200px;
  width: 10vw;
  margin: 20px;
  margin-bottom: 50px;
  border-radius: 20px;
  opacity: ;
}
.navigate{
  border-radius: 20px;
  background: transparent;
}
.header{
  height: 400px;
  width: 80%;
  border-radius:25px;
  margin-top: 50px;
}
video{
  position: absolute;
  margin-top: -60px;
  margin-left: -25px;
  height: 400px;
  border-bottom-left-radius: 25px;
  border-bottom-right-radius: 25px;
  object-fit: cover;
  width: 74.2vw  !important;
  opacity: ;
}
.nav-content {
  color: black;
  padding: 10px 20px;
  position: relative;
  text-align: center;
  border-bottom: 3px solid transparent;
  display: flex;
  left: 0;
  padding: auto;
}
.navlinks {
  color: #fff;
  padding: 1px 20px;
  position: relative;
  text-align: center;
  border-bottom: 1px solid transparent;
  display: flex;
  float: right;
  transition: width 4.4s;
}
a {
  text-decoration: none;
  color: white;
}
.navlinks.active,
a:hover,
.navlinks:hover {
  color: #421A4C;
  border-bottom-color: #421A4C;
  transition: width 2.4s linear;
  transition-property: border-bottom;
}

@media only screen and (max-width: 768px) {
  video{
  position: absolute;
  margin-top: -12px;
  margin-left: -12px;
  height: 200px;
  border-bottom-left-radius: 25px;
  border-bottom-right-radius: 25px;
  object-fit: cover;
  width: 92.5vw  !important;
  opacity: ;
  }


}
</style>