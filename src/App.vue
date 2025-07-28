<script setup>
import { ref } from 'vue'

const text = '這是一段文字' //原始型別

const text2 = ref('還是一段文字') //物件型別

let num0 = 0

let num = ref(0)

let num1 = '1'

let num2 = ref('2')

setInterval(()=>{
  num.value++
},500)

const htmlTemplate = '<html><head><title>OXXO.STUDIO</title></head><body><p>我是內容</p></body></html>'

</script>

<template>
  <div>
     {{ text }}
     {{ typeof text}}
     <hr>
     {{ text2 }}
     {{ typeof text2 }}
     <hr>
     {{ num0 }}
     {{ typeof num0 }}
     <hr>
     <p>這個數值目前是:{{ num }}</p>
     {{ typeof num }}
     <h1 v-text="num"></h1>
     <hr>
     {{ num1 }}
     {{ typeof num1 }}
    <hr>
    {{ num2 }}
    {{ typeof num2 }}
    <hr>
     <h1>雙花括號</h1>
     {{ htmlTemplate }}
     <hr>
     <h1>v-text</h1>
     <div v-text="htmlTemplate"></div>
     <hr>
     <h1>v-html</h1>
     <div v-html="htmlTemplate"></div>
     <p class="alert">XSS 手法之一，不要輕易使用!</p>
     <input value="<script>alert('Hacked!')</script>">

  </div>
</template>
<style>

.alert {
  color:red;
  font-weight: 900;
  font-size: larger;

}


</style>
