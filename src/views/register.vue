<template>
    <div class="login">
    <Main />
    <Form />
  </div>

</template>

<script lang="ts">
import Main from  '../components/main.vue'
import Form from '../components/signupForm.vue'

export default {
  components: {
    Main,
    Form
  },
}
</script>


<style>
.login{
  position: absolute;
  height: 200vh;
  width: 100vw;
  background-size: cover;
  background-image: url("../assets/background.png");
}
</style>