<template>
    <Header text="header"></Header>
  <p>Ini Dari NewComponent</p>
  <MyComponent nama="ucup" umur="18"/>
  <hr>
  <Umur nama="ujang" umur="18"></Umur>
  <hr>

  <LatihanDuaComponent></LatihanDuaComponent>
  <hr>
  <ComponentWatchers nama="nanang" umur="11"></ComponentWatchers>
  <EventComponent :name="nama" :umur="umur" @greeted="onGreeted"></EventComponent>


  </template>
  
  <script setup>
  import EventComponent from './EventComponent.vue';
  import ComponentWatchers from './ComponentWatchers.vue';
  import LatihanDuaComponent from './LatihanDuaComponent.vue';
  import Header from '../components/header.vue'
  import MyComponent from '../components/MyComponent.vue'
  import Umur from '../components/umur.vue';
  // event
  import { ref } from 'vue';
const nama = ref('John');
const umur = ref(25);
const onGreeted = () => {
    console.log('Kamu udah disapa, bro!');
};
 
  </script>