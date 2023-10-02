<template>
  <!-- <TemplateRef /> -->
  <!-- <RefWithWatch /> -->
  <!-- <RefWithVfor /> -->
  <!-- <RefWithFunction /> -->
  <RefWithComponent ref="componentRef"/>
  <button @click="parentIncrease()"> parent refer child</button>
</template>
 
 
<script setup>
 
import { ref, reactive, computed ,onMounted } from 'vue'
// import TemplateRef from './TemplateRef.vue'
// import RefWithWatch from './RefWithWatch.vue'
// import RefWithVfor from './RefWithVfor.vue'
// import RefWithFunction from './RefWithFunction.vue'
 
import RefWithComponent from './RefWithComponent.vue'
 
//  ref on component

const componentRef = ref(null);
const funcVal = ref(null);
onMounted(()=>{
  console.log("component ref",componentRef.value.count);
  funcVal = ref(componentRef.value.count);
})
function parentIncrease()
{
  if(componentRef.value){
      componentRef.value.increaseCount();
  }

}
</script>
 
<style scoped>
 
</style>