<template>
  <div>
    <button v-on:click="upFunction" class="btn "><img src="./img/t1.gif" width="70" height="70">{{lable}}</button>
    <button v-on:click="downFunction" class="btn ml-3"><img src="./img/t2.gif" width="55" height="55">{{lable}}</button>
    <button v-on:click="LoveFunction" class="btn ml-3"><img src="./img/t3.gif" width="70" height="70"> {{lable}}</button>
    <button v-on:click="ResetFunction" class="btn ml-3"><img src="./img/t4.png" width="70" height="70">{{lable}}</button>


  </div>
</template>
<script>
export default {
  data: function () {
    return {
      counter: 0,
    };
  },
  props: {
    lable: String,
  },
  methods: {
    upFunction: function () {
      this.counter += 1;
      this.$emit("cc", this.counter);
    },

    downFunction: function () {
      this.counter += -5;
      this.$emit("cc", this.counter);
    },

    LoveFunction: function () {
      this.counter += 10;
      this.$emit("cc", this.counter);
    },

    ResetFunction: function () {
      this.counter = 0;
      this.$emit("cc", this.counter);
    },
  },
};
</script>
<style>
</style>