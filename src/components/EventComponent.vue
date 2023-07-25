<template>
  <div>
    <h1>Aplikasi Vue.js Gue</h1>
    <my-component
      :nama="nama"
      :umur="umur"
      @greeted="onGreeted"
    >
      <p>Ini konten tambahan dalam slot</p>
    </my-component>
  </div>
</template>

<script>
import MyComponent from './MyComponent.vue';

export default {
  components: {
    MyComponent
  },
  data() {
    return {
      nama: 'John',
      umur: 25
    };
  },
  methods: {
    onGreeted() {
      console.log('Kamu udah disapa, bro!');
    },
    greet() {
            console.log('Halo, bro!');
            this.$emit('greeted'); // Memancarkan event 'greeted'
        }
  }
  
}
</script>