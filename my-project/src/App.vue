<script setup>
import {ref, onMounted} from 'vue';
import ChildComp from './components/ChildComp.vue';

let count = ref(0); //상태변수 초기값 (state)
let title = "Hello Vue";

onMounted(()=> {
  console.log('mounted');
})

const increaseCount = () => {
  count.value++;
}
</script>

<template>
 <div>
  <h1>App</h1>
  <button @click="increaseCount">count++</button>
  <p>{{  count }}</p>
  <ChildComp color="red"/>
 </div>
</template>

<style scoped>

</style>
