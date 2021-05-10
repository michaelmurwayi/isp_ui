<template>
  <v-card round class="form">

    <v-card-title style="background-color:rgb(0,0,0, 0.8); height:80px;" primary-title>
      <p style="color:white; margin-left:200px;"> Customer Registration </p>
      </v-card-title>
         <v-form
    ref="form"
    v-model="valid"
    dark
  >
    <v-text-field
    class="text-field"
      v-model="name"
      :counter="10"
      :rules="nameRules"
      label="First Name"
      required
    ></v-text-field>
    <v-text-field
    class="text-field"
      v-model="name"
      :counter="10"
      :rules="nameRules"
      label="Last Name"
      required
    ></v-text-field>

    <v-text-field
    class="text-field"
      v-model="email"
      :rules="emailRules"
      label="Username"
      required
    ></v-text-field>

    <v-text-field
    class="text-field"
      v-model="email"
      :rules="emailRules"
      label="E-mail"
      required
    ></v-text-field>
    <v-text-field
    class="text-field"
      v-model="name"
      :counter="10"
      :rules="nameRules"
      label="Phonenumber"
      required
    ></v-text-field>

    <v-text-field
    class="text-field"
      v-model="email"
      :rules="emailRules"
      label="Password"
      required
    ></v-text-field>

    <v-checkbox
    class="text-field"
      v-model="checkbox"
      :rules="[v => !!v || 'You must agree to continue!']"
      label="Do you agree?"
      required
    ></v-checkbox>

    <v-btn
      color="dark"
      class=" ml-4 mr-4"
      @click="reset"
    >
      Register
    </v-btn>

    <v-btn
      color="success"
      @click="resetValidation"
    >
      Already have Account?
    </v-btn>
  </v-form>
  </v-card>   
</template>


<script>
  
</script>

<style scoped lang="scss">
.form{
  position:absolute;
  left:500px;
  width: 600px;
  height: 1000px;
  top:60vh;
  border-radius:30px;
}
.text-field{
  color: white  !important;
  margin: 40px;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
