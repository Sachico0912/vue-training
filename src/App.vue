<script setup>
import { ref } from 'vue'
// v-on: 像監聽器的魔法?
// 縮寫 @

const handleClick = ()=>{
  console.log("我被觸發了")
}

const submitForm = ()=>{
  console.log("表單被觸發了")
}

const text = ref('這是一段文字')

</script>

<template>
  <div><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
    <form action="" @submit.prevent="submitForm">
    <button type="button" v-on:click="handleClick">type="button"按鈕</button>
    <p>當按鈕存在於表單內時，預設行為會送出並刷新頁面，所以需要使用type="button"</p>
    <button @click="handleClick">沒有type的按鈕</button>
    <button type="submit">type="submit"按鈕></button>
    </form>

    <h2>事件修飾符</h2>
    <a href="#" @click="handleClick">我是連結</a>
    <p>a連結#會跳到特定id位置，如果沒有特定位置就會回到最上面</p>
    <a href="#" @click.prevent="handleClick">我是連結清除預設行為</a>

    <h2>按鍵修飾符</h2>
    <input type="text" @keydown.enter="handleClick" v-model="text">
  </div>
</template>
<style>


</style>
