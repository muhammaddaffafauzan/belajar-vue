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
let b = 20;
let c = a + b;
// pengulangan
let number = 1;
let data = [
  { 
    nama: 'useng',
   kelas: 'XII RPL 1',
   alamat: 'bandung'
  },
  {
   nama: 'asep',
   kelas: 'XII RPL 2' ,
   alamat: 'garut'
  },
  {
   nama: 'agus',
   kelas: 'XII TKR 2' ,
   alamat: 'inggris'
  },
  {
   nama: 'nanang',
   kelas: 'XII TSM 2' ,
   alamat: 'new york'
  },
  {
   nama: 'mamat',
   kelas: 'XI TKR 2' ,
   alamat: 'gotham city'
  },
]
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
 <a :href="url">ini link pendaftaran nya</a>
 {{ msg.split('').reverse().join(' ')
}}<hr>
 <h1>{{ art }}</h1>
<br> bilangan {{ a }} dijumlahkan bilangan {{ b }} maka hasilnya adalah {{ c }}
</form>
<hr>
<h1>data siswa</h1>
<table border="1" >
  <tr>
    <th>No</th>
    <th>nama siswa</th>
    <th>kelas</th>
    <th>alamat</th>
  </tr>
  <tr v-for ="siswa in data">
  <th>{{ number++ }}</th>
  <td> {{ siswa.nama }} </td>
  <td>{{ siswa.kelas }}</td>
  <td>{{ siswa.alamat }}</td>
  </tr>
</table>
</div>
</template>