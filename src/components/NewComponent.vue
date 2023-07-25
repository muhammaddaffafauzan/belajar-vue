<template>
  <div>
    <Header text="header"></Header>
  <p>Ini Dari NewComponent</p>
  <MyComponent nama="ucup" umur="18"/>
  <hr>
  <Umur nama="ujang" umur="18"></Umur>
  <hr>

  <LatihanDuaComponent></LatihanDuaComponent>
  <hr>
  <ComponentWatchers nama="nanang" umur="11"></ComponentWatchers>
  <EventComponent :nama="nama" :umur="umur" @greeted="onGreeted">
            <template #footer>
                <div>
                    <p>Ini Adalah Footer Latihan Event</p>
                </div>
            </template>
            <template #header>
                <div>
                    <p>Ini Adalah Header latihan Event</p>
                </div>
            </template>
        </EventComponent>
    </div>

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