<template>
     <h2 v-for="(student,i) in students" :key=i :ref="(el)=>{elements[i] = el}" >{{student}}</h2>

</template>
 
 
<script setup>
 
import { ref, reactive, computed,onMounted  } from 'vue'
  const students = ref(['sonam','rahul','sagar']) 
  const elements = ref([]);
  
onMounted(()=>{
    console.log('elements',elements.value[0].innerHTML)
})
</script>
 
<style scoped>
 
</style>