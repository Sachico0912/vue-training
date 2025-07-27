<script setup>
import { ref } from 'vue'

//v-for
//v-if
//v-show

const array = ref([
  {
  id:'1',
  name: '小明',
  age: 18 
  },
  {
  id:'2',
  name: '小美',
  age: 16 
  },
  {
  id:'3',
  name: '大仁',
  age: 20 
  },
])

const isChecked = ref(false)

</script>

<template>
  <div>
    <div>
      姓名:{{ array[0].name }}
      年齡:{{ array[0].age }}
    </div>
    <hr>
    // v-for 必須加上:key
    <div v-for="(item, key) in array" :key="item.id">
      索引:{{ key }}
      姓名:{{ item.name }}
      年齡:{{ item.age }}
      <div v-if="item.age > 18">大於 18 歲</div>
      <div v-else>小於 18 歲</div>
      
    </div>
    <hr>
    <input type="checkbox" v-model="isChecked">{{ isChecked }}
    
    <b v-if="isChecked">當 isChecked == true 會顯示這行</b>
    <b v-else="isChecked">目前的 isChecked == false</b>
    <hr>
    <b v-show="isChecked">v-show 目前的 isChecked == true</b>

  </div>
</template>
<style>


</style>
