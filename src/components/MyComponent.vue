<template>
  <p>Ini dari MyComponent</p>
  <p> Nama :{{ nama }}</p>
  <p> Umur :{{ umur }}</p>
  <p> jenis kelamin :{{ jk }}</p>
</template>

<script>  
export default {
  name: 'MyComponent',
  props: ['nama', 'umur'],
  data(){
    return{
      jk:'laki-laki'
    }
  }
}
</script>