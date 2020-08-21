<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
  
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
   data: function() {
return {
    counter: 0
  };
}
}
</script>


<style scoped>
  .hello{
    
    text-align: center;
  }
</style>
