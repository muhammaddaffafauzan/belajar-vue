<template>
    <Header text="header"></Header>
  <p>Ini Dari NewComponent</p>
  <MyComponent nama="daffa" umur="18"/>
  <hr>


  <Umur nama="ujang" umur="18"></Umur>
  <hr>
  <LatihanDuaComponent></LatihanDuaComponent>
  </template>
  
  <script>
  import LatihanDuaComponent from './LatihanDuaComponent.vue';
  import Header from '../components/header.vue'
  import MyComponent from '../components/MyComponent.vue'
  import Umur from '../components/umur.vue';
  export default{
    components : {
    MyComponent,
    Header,
    Umur,
    LatihanDuaComponent
},
    data(){
    return{
      alamat: 'bandung'
    }
  }
  
  }
  </script>