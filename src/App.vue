<script setup>
import { ref } from 'vue'

let msg = "Mau masuk pemuda pancasila gak?"
let art = "Sekarang aritmatika"
let rawHtml = "<li>tampang sangar</li><li>bisa malak</li><li>parkir/pungli</li>"
const objectOfAttrs = {
  id: 'container',
  class: 'wrapper'
}
let seen = " "
// aritmatika
let a = 10;
let b = 5;
let c = a + b;
</script>
<template>
<div>
  
 <form @submit.prevent="onSubmit">
  <h1>{{ msg }}</h1>
 <div v-bind="objectOfAttrs">syaratnya:</div>
 <span v-html="rawHtml"></span>
 <p v-if="seen">kalo mau itu juga ya, gaji 3 digit 300 perak</p>
 <button :disabled="isButtonDisabled" onclick="alert('SELAMAT ANDA MASUK PEMUDA PANCASILA :)')">ya aku mau</button>&ensp;
 <button :disabled="isButtonDisabled" onclick="confirm('gamau tau kamu harus masuk aku maksa nih!!')">Gak mau</button><br>
 <a :href="url">ini link pendaftaran nya</a><hr>
 <h1>{{ art }}</h1>
<br> bilangan {{ a }} dijumlahkan bilangan {{ b }} maka hasilnya adalah {{ c }}
</form>
</div>
</template>