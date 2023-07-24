<template>
  <div>
 <Header text="ini adalah header"></Header>
    <h2>Ini aplikasi Vue.js gue!</h2>
    <my-component nama="John" umur="25"></my-component>
  </div>
</template>

<script>
import MyComponent from './components/Mycomponent.vue'; // Import komponen yang udah kita buat
import Header from './components/header.vue';
export default {
  components: {
    MyComponent, // Daftarkan komponen agar bisa digunakan di sini
    Header
  },
}
</script>
