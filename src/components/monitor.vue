<template>
<v-app>
    <v-flex  class=""  v-for="items in titles" :key="items">
          <v-card dark class="monitor  col-md-12   ma-5  text-center " shaped elevation="10">
            <div class="row">
            
            <v-avatar class="mt-10  ml-15 col-md-3" style="margin-left:400px;" size="80" elevation="10">
              <img src="img8.jpg" />
            </v-avatar>

            <v-card-title class="layout justify-left ">
              <p> {{ items.title }} </p>
                </v-card-title>
            </div>
              <hr class="hr">
            <v-card-subtitle class="layout justify-right"> {{ items }} </v-card-subtitle>
          </v-card>
        </v-flex>   
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
    position: relative;
    top: 80px;
    height: 250px;
    width: 600px;
}
.hr {
  border: 10px solid green;
  border-radius: 5px;
  margin-top: 50px;
}
</style>