<template>
<div class="btn-dark">
  <HelloWorld msg=" Warriors " />
 <div id="app">
   
    <div class="row container-fluid">
      <div class="col-6">
        <img alt="Vue logo  " src="./assets/vos.jpg" width="500" height="700"/>
      </div>
      <div class="col-6">
        <img alt="Vue logo  "  src="./assets/vow.jpg" width="500" height="700"/>
      </div>
    </div>
    <hr>
    <div class="row">
      <div class="col-6">
        <h1>{{total1}}</h1>
      </div>
      <div class="col-6">

        <h1>{{total2}}</h1>
      </div>
      <div class="col-6">
        <CsBotton @cc="sum" />
      </div>
      <div class="col-6">
        <CsBotton @cc="sum1" />
      </div>
    </div>
    
  </div>
</div>
</template>
<script>
import HelloWorld from "./components/HelloWorld.vue";
import CsBotton from "./components/CsBotton.vue";
export default {
  name: "App",
  components: {
    HelloWorld,
    CsBotton,
    
  },
  data : function(){
    return {
    total1: 0,
    total2: 0,
   
   } 
  },
  methods: {
  sum(counterValue){
    this.total1 = counterValue
  },
  
  sum1(counterValue){
    this.total2 = counterValue
 
  
},
},

};

</script>

<style>
#app {
  
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: white;
  margin: auto;
}
</style>