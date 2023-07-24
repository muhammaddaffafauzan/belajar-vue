<template>
  <div>
    <h1>Halo, dunia!</h1>
    <p>Ini komponen buatan gue.</p>
    <h2>Halo, {{ nama }}!</h2>
    <p>Umur kamu: {{ umur }}</p>
  </div>
</template>


<script>
export default {
  name: 'MyComponent', // Nama komponen, bisa diubah sesuai kebutuhan
  props: ['nama', 'umur'], // Definisi props "nama" dan "umur"
  // Data komponen
  data() {
    return {
      message: 'Ini pesan dari komponen!'
    };
  },
  // Metode-metode komponen
  methods: {
    greet() {
      console.log('Halo, bro!');
    }
  }
}
</script>


<style>
h1 {
  color: blue;
}

p {
  font-size: 16px;
}
</style>
