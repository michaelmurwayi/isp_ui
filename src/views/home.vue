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

      <v-app-bar-title class="mask pattern-8">SwiftNet</v-app-bar-title>

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
          <div ><router-link class="navlinks" to="products" style="color:white"> Login</router-link></div>
          <div ><router-link class="navlinks" to="services" style="color:white"> Register</router-link></div>
          <div ><router-link class="navlinks" to="about" style="color:white"> Account</router-link></div>
        </div>
      </v-flex>
    </v-div>
      </template>
    </v-app-bar>

  </v-card>
    <!-- end of page navigation div -->

   
    <!-- end of header div -->

    <!-- begin of page intro -->
  <div>
  <div class="col-md-12 text-center">
    <v-carousel
    class="intro"
    cycle
    height="200"
    hide-delimiters
    :show-arrows="false"
  >
    <template v-slot:prev="{ on, attrs }">
      <v-btn
        color="success"
        v-bind="attrs"
        v-on="on"
      >Previous slide</v-btn>
    </template>
    <template v-slot:next="{ on, attrs }">
      <v-btn
        color="info"
        v-bind="attrs"
        v-on="on"
      >Next slide</v-btn>
    </template>
    <v-carousel-item
      v-for="(slide, i) in slides"
      :key="i"
    >
      <v-sheet
        :color="colors[i]"
        height="100%"
      >
        <v-row
          class="fill-height"
          align="center"
          justify="center"
        >
          <div class="display-3">
            {{ slide }} Slide
          </div>
        </v-row>
      </v-sheet>
    </v-carousel-item>
  </v-carousel>
  </div>
  </div>
    <!-- end of page intro -->
  </v-container>
    </v-container>
  </v-app>
</template>

<script>
export default {
   data () {
      return {
        colors: [
          'indigo',
          'warning',
          'pink darken-2',
          'red lighten-1',
          'deep-purple accent-4',
        ],
        slides: [
          'First',
          'Second',
          'Third',
          
        ],
      }
    },
  }
</script>

<style>
.main{
  background-image: url("../assets/background.png");
  position: absolute;
  bottom: 0px;
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
  font-family:Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
  font-size: 2vh;
  font-weight: 200px;
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
.intro{
  position: absolute;
  background: transparent;
  top:165px;
  left: 0px;
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