<template>
  <div>
    <h3>{{ text }}</h3>
  </div>
</template>
<script>
export default {
  name: "Header",
  props: ['text']
}
</script>
<style>
h3{
  text-align: center;
  color: black;
  background-color: cadetblue;
}
</style>