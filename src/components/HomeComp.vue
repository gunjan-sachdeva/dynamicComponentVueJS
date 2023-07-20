<template>
  <h1>Dynamic components</h1> 
  <button @click="tab='JavaComp'">Load Java</button> 
  <button @click="tab='NodeComp'">Load Node Js</button>
  <button @click="tab='PhpComp'">Load Php</button>

  <component :is="tab" />
  <!-- <JavaComp />
  <PhpComp />
  <NodeComp /> -->

</template>
<script>
import JavaComp from './JavaComp.vue'

import PhpComp from './PhpComp.vue'
import NodeComp from './NodeComp.vue'


export default {
    name:"HomeComp",
    components:{
      JavaComp,
      PhpComp,
      NodeComp
    },
    data()
    {
      return{
        tab:'JavaComp'
      }
    }
}
</script>
<style scoped>

</style>