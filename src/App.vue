<script setup>
import { ref } from 'vue'
// import HelloWorld from './components/HelloWorld.vue'
// 雙向綁定
const text = ref('這是一段文字')
const city = ref('台北市')
const isChecked = ref(true)
const arrayCheckbox = ref([])
const radioValue = ref('男')
</script>

<template>
  <div>
    <h1>{{ text }}</h1>
    <input type="text" v-model="text">
    <hr>
    {{ city }}
    <select name="" id="" v-model="city">
      <option value="0">台北市</option>
      <option value="1">台中市</option>
      <option value="2">高雄市</option>
    </select>
    <hr>
    {{ isChecked }}
    <input type="checkbox" v-model="isChecked">
    <hr>
    {{ arrayCheckbox }}
    <input type="checkbox" v-model="arrayCheckbox" value="小姐姐">
    <input type="checkbox" v-model="arrayCheckbox" value="小哥哥">
    <input type="checkbox" v-model="arrayCheckbox" value="漂亮阿姨">
    <hr>
    {{ radioValue }}
    <input type="radio" v-model="radioValue" value="南">
    <input type="radio" v-model="radioValue" value="女">
  </div>
</template>

