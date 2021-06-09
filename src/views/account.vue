<template>
<v-app class="main">
  <div style="position:absolute; top:0px;" class="col-md-12">
    <sideNav />
  </div>
  <div class="ml-n2">
  <Monitor class="monitor mt-15" :titles="titles"/>
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
  background-color: blanchedalmond;
}
.main{
  background-image: url("../assets/background.png");
  background-size: cover;
  position: absolute;
  top: 0px;
  bottom: 0px;
  height: 160%;
  width: 100%;
  border-radius: 0px;
  background-color: red;
}
</style>