<script setup>
import { ref } from 'vue'

const imgUrl = ref('https://images.unsplash.com/photo-1682685796063-d2604827f7b3?q=80&w=300&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDF8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D')
const isChecked = ref(false)
</script>

<template>
  <div>
   <img v-bind:src="imgUrl" alt="">
   <h2>v-bind:可以套用在任何屬性上</h2>
   <h2>:黑魔法?</h2>
   {{ isChecked }}
   <input type="checkbox" v-model="isChecked">
   <input type="text" :disabled="isChecked">
   <h2>可以套用在行內樣式上</h2>
  <div 
   class="box" 
   v-bind:style="{ transform: isChecked ? 'rotate(45deg)': null }">
  </div>
  <hr>
  <div 
   class="box" 
   v-bind:style="{ backgroundColor: isChecked ? 'red' : 'green' }">
  </div>
  <h2>class</h2>
  <div class="box" :class="{ rotate : isChecked }"></div>

  </div>
</template>
<style>

.box {
  height: 100px;
  width: 100px;
  background-color: red;
  transition: .5s all;
}

.rotate {
  transform: rotate(45deg);
}
</style>
