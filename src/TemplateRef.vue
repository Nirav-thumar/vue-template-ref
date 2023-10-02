<template>
    <div>
        <label for="userName">User Name </label>
        <input type="text" id="userName" ref="inputRef">
    </div>
</template>
 
 
<script setup>
 
import { ref, reactive, computed,onMounted  } from 'vue'
 
const inputRef = ref('sonam');

    console.log('name',inputRef.value)
onMounted(()=>{
    console.log("onMounted",inputRef.value)
    inputRef.value.focus();
})
</script>
 
<style scoped>
 
</style>