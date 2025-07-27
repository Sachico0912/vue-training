<script setup>
import { ref } from 'vue'

const message = ref('這是一串訊息')

const number1 = ref(1)

const number2 = ref('2')

const checkboxArray = ref([])

const singleRadio = ref([])

</script>

<template>
  <div>
    <input type="text" v-model="message">
    {{ message }}
    <hr>
    <input type="text" v-model.lazy="message">
    {{ message }}
    <hr>
    <input type="text" v-model.trim="message">
    {{ message }}
    <hr>
    <input type="text" v-model.number="number1">
    {{ number1 }}
    {{ typeof number1 }}
    <hr>
    <input v-model="number1">
    {{ number1 }}
    {{ typeof number1 }}
    <hr>
    <input type="text" v-model="number2">
    {{ number2 }}
    {{ typeof number2 }}
    <hr>
    {{ checkboxArray }}
    <div class="form-check">
      <input type="checkbox" class="form-check-input" id="check1" v-model="checkboxArray" value="雞">
      <label class="form-check-label" for="check1">雞</label>
      <input type="checkbox" class="form-check-input" id="check2" v-model="checkboxArray" value="豬">
      <label class="form-check-label" for="check2">豬</label>
      <input type="checkbox" class="form-check-input" id="check3" v-model="checkboxArray" value="牛">
      <label class="form-check-label" for="check3">牛</label>
    </div>
    <hr>
    您選擇了:{{ singleRadio }}
    <div class="form-check">
      <input type="radio" class="form-check-input" id="radio1" v-model="singleRadio" value="雞">
      <label class="form-check-label" for="radio1">雞</label>
      <input type="radio" class="form-check-input" id="radio2" v-model="singleRadio" value="豬">
      <label class="form-check-label" for="radio2">豬</label>
      <input type="radio" class="form-check-input" id="radio3" v-model="singleRadio" value="牛">
      <label class="form-check-label" for="radio3">牛</label>
    </div>

  </div>
</template>
<style>


</style>
