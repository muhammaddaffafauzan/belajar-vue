<template>
    <Header text="well"></Header>
  <p>Ini Dari NewComponent</p>
  <MyComponent nama="daffa" umur="18"/>
  <p>alamat :{{ alamat }}</p>
  </template>
  
  <script>
  import Header from '../components/header.vue'
  import MyComponent from '../components/MyComponent.vue'
  export default{
    components : {
      MyComponent,
      Header
    },
    data(){
    return{
      alamat: 'bandung'
    }
  }
  
  }
  </script>