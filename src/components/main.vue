<template>
  <div>
        <v-container class="container-fluid">
          <div>
    <!-- start of navigation div -->
    <v-card class="navigate">
    <v-app-bar
      color="#6A76AB"
      dark
      height="200"
      prominent
      class="navigation"
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
         <div class="navigate mt-4">
        <v-flex class="subnav-content">
        <div class="nav-content">
          <div ><router-link class="navlinks" to="/" style="color:white">Home</router-link></div>
          <div ><router-link class="navlinks" to="login" style="color:white"> Login</router-link></div>
          <div ><router-link class="navlinks" to="Register" style="color:white"> Register</router-link></div>
          <div ><router-link class="navlinks" to="Account" style="color:white"> Account</router-link></div>
        </div>
      </v-flex>
    </div>
      </template>
    </v-app-bar>
    </v-card>
  <!-- end of page navigation div -->
  </div>
        </v-container>
  </div>
</template>

<script>
  
</script>

<style scoped>
.container-fluid{
  background:	#E8E8E8;
  height: 130vh;
  position: absolute;
  top: 100px;
  left: 200px;
  margin: 20px;
  margin-bottom: 50px;
  border-radius: 20px;
  box-shadow: 5px 5px 5px 5px black;
}
.navigate{
  border-radius: 20px 20px 0px 0px ;
  top: 0px;
  left: 0px;
  right: 0px;
  margin-left: px;
  width: 800vw !important;
  position: absolute;

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
</style>