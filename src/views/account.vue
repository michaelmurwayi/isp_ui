<template class="">
<v-app>

  <div style="position:absolute; top:0px;" class="col-md-12">
    <sideNav />
  </div>
  <div class="row mt-5">

  <div class="monitor col-md-5 red">
    
  </div>

  <div class="monitors col-md-6 ">

    <Monitor class="monitor" :titles="titles"/>
  </div>
  </div>

</v-app>
</template>

<script lang="ts">
import sideNav from  '../components/sideNav.vue'
import Monitor from  '../components/monitor.vue'

export default {
  components: {
    sideNav,
    Monitor
  },
  data () {
    return {
      titles: [
        {title:'Connection Status'},
        {title:'Purchased'},
        {title:'Bundle'},
      ]
    }
    }
  }
</script>


<style>
.account_main{

  background-image: url('../assets/account_background.jpeg');
}
.monitor{
  height:100px;
  position: relative;
  top: 200px;
  margin-left: 20px;
}
.monitors{
  position: relative;
  margin-top: 0px;
  margin-left: 20px;
  height: 100vh;
}
</style>