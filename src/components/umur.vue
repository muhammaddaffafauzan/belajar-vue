<template>
  <div>
    <h2 v-if="umur >= 18">Selamat datang, {{ nama }}!</h2>
    <p v-else>Maaf, kamu belum cukup umur.</p>
    <button @click="greet">Sapa Bro!</button>
  </div>
</template>
<script>
export default {
  props: ['nama', 'umur'],
  data() {
    return {
      pesan: 'Halo, ' + this.nama + '!'
    };
  },
  methods: {
    greet() {
      alert('Halo ' + this.nama);
    }
  },
  computed: {
    pesanSelamat() {
      return 'Selamat datang, ' + this.nama + '!';
    }
  }
}
</script>