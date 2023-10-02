<template>
    <div>
        <label for="userName">User Name </label>
        <input type="text" id="userName" ref="inputRef">
    </div>
</template>
 
 
<script setup>
 
import { ref, reactive, computed,onMounted ,watchEffect } from 'vue'
 
const inputRef = ref(null);

watchEffect(()=>{
    console.log('watchEffect')
    console.log('inputRef value',inputRef.value)
    if(inputRef.value){
        console.log(inputRef.value);
        inputRef.value.focus();
    }
    else{
        console.log('not mounted')
    }
})
</script>
 
<style scoped>
 
</style>