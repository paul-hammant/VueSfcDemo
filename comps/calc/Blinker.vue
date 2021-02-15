<template>
  <div ref="blinkerRef" id="cursory">
  </div>
</template>

<script>
import Velocity from "https://unpkg.com/velocity-animate@1.5.2/velocity.min.js";

export default {
  name: 'blinker',
  mounted:function(){
    this.onLoady()
  },
  methods: {
    onLoady: function() {
      Velocity(this.$refs.blinkerRef, {opacity: 0}, {loop: true});
    }
  }
}

</script>

<style>
#cursory {
  width: 5px;
  height: 60px;
  background-color: black;
}

</style>
