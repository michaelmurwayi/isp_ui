<template>
  <v-app>
    <v-container
    fluid
    class="main"
    >
    <!-- start of navigation div -->
    <v-app-bar rounded class="navigation mt-4">
       <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-toolbar-title>Title</v-toolbar-title>

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
    </v-app-bar>
    <!-- end of page navigation div -->

    <!-- start of header div -->
    <div class="container-fluid mask pattern-8 header col-md-12">
      <video autoplay muted loop class="mask pattern-8">
      <source src="../assets/header.mp4"  type="video/mp4">
    </video>
    </div>
     <v-toolbar app flat fixed color="transparent" prominent >
      <v-card-text class="px-0">
      <v-btn flat solo outlined color="black" class="mr-2 white"><strong>Home</strong></v-btn>
      <v-btn flat outlined color="black" class="mr-2 white"><strong>Register</strong></v-btn>
      <v-btn flat outlined color="black" class="mr-2 white"><strong>Login</strong></v-btn>
      <v-btn flat outlined color="primary" class="mr-2"><strong>Account</strong></v-btn>
      </v-card-text>    
    </v-toolbar>
    <!-- end of header div -->
    </v-container>
  </v-app>
</template>

<script>
export default {
  
}
</script>

<style>
.main{
  background-color: #28313b;
  height: 100vh;
  border-radius: 0px;
}
.navigation{
  border-radius: 20px;
}
.header{
  height: 400px;
  width: 550px;
  border-radius:25px;
  margin-top: 0px;
}
video{
  position: absolute;
  margin-top: -12px;
  margin-left: -12px;
  height: 400px;
  border-bottom-left-radius: 25px;
  border-bottom-right-radius: 25px;
  object-fit: cover;
  width: 97.5vw  !important;
  opacity: ;
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