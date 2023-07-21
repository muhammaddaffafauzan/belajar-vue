<style>
h1{
  color: red
}
p{
  font-size: 16px;
}
</style>
<template>
  <div>
    <h2>Formulir</h2>
    <form @submit.prevent="submitForm">
    <label for="">nama</label>
    <input type="text" name="nama" v-model="kontak.nama"><br>
    <label for="">Email</label>
    <input type="email" name="email" v-model="kontak.email"><br>
    <input type="submit" value="simpan">
    <div id="a"></div>
    </form>
  </div>
</template>
<script>
export default {
  name:  'Mycomponents', // Nama komponen, bisa diubah sesuai kebutuhan
// Data komponen
  data() {
     return {
        kontak :[
        { nama: '',
        email: ''}
      ]
     };
  },
// Metode-metode komponen
  methods: {
   submitForm(){
    document.getElementById('a').innerHTML += ("<br>nama: " + this.kontak.nama) + ("<br>Email :" + this.kontak.email)
   }
  }
};
</script>