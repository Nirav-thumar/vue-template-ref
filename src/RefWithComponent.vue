<template>
 <h2>Child Component</h2>
 count {{count}}
 a {{a}}
 <button @click="increaseCount">increaseCount</button>
</template>
 
 
<script setup>
 
import { ref, reactive, computed  } from 'vue'
 const count = ref(10);
 const a= 20;
 function increaseCount(){
    count.value++;
 }
 defineExpose({
    count,
    a,
    increaseCount,
})
</script>
 
<style scoped>
 
</style>