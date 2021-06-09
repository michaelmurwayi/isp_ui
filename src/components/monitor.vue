<template>
<v-app>
    <div class="">
    <div class="col-md-12 row">
      <div  v-for="items in titles" :key="items" class="ml-2">

          <v-card color="#385F73" class=" ma-10 text-center col-md-12" shaped elevation="10">
            <div class="row">
            
            <v-avatar class="mt-10  ml-2 col-md-3" size="60" elevation="10">
              <img src="img8.jpg" />
            </v-avatar>

            <v-card-title class="layout justify-left text-white" style="">
              <p> {{ items.title }} </p>
                </v-card-title>
            </div>
            <v-card-subtitle class="layout justify-right text-white"> {{ items }} </v-card-subtitle>
          </v-card>
      </div>
    </div>
          <hr class="hr mt-15">
          <v-card-title class="text-grey ml-15"> {{ titles[0].title }} :<v-card-title class="text-green"> Connection is Limited Please Purchase a Data Plan</v-card-title> </v-card-title>
          <hr class="hr mt-n4">
  </div>
          
</v-app>
</template>

<script>
export default {
  props: {
  titles: Array,
},
  data () {
    return {
      bundles: [
        'First',
        'Second',
        'Third',
        
      ],
    }}
  }
</script>

<style scoped>
.monitor{
    position: absolute;
    top: 200px;
    height: 250px;
    width: 100vw;
}
.hr {
  /* border: 10px solid black; */
  border-top: 4px dashed black;
  opacity: 0.7;
  border-radius: 5px;
  margin-top: 50px;
}
.v-card{
  width: 420px;
  background-image: url("https://picsum.photos/1920/1080?random");
}
</style>