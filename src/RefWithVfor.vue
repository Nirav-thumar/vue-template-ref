<template>
    <h2 v-for="(student,i) in students" :key=i ref="studentsRef" >{{student}}</h2>
</template>
 
 
<script setup>
 
import { ref, reactive, computed ,onMounted } from 'vue'
 
 const students = ref(['sonam','rahul','sagar']) 
 const studentsRef = ref([]);

onMounted(()=>{
    console.log("studentRef : ",studentsRef.value)
})


</script>
 
<style scoped>
 
</style>