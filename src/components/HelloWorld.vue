<template>
  <v-app>

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

  </v-app>
</template>

<script>
  
</script>

<style scoped>

</style>