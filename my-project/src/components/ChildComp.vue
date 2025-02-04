<template>
    <div>
        <h2>Child Component</h2>
        <p :style="{color : color}">{{ color }}</p>
    </div>
</template>
<script setup>
const props = defineProps({
    color:String,
})
console.log(props.color);
</script>
<style>
    
</style>