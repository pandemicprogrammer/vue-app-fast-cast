
// APP TEMPLATE
<template>
 
    <FastCast />
  </template>


// JAVASCRIPT
<script>

import FastCast from './components/FastCast.vue'

export default {
  // Options Object
  name: 'App',
  components: {
    FastCast
  }
}
</script>


// STYLES

<style>
.container {
  border: solid gray;
  max-width: 26rem;
  display:  block;
justify-content: center;
}
.logo {
  max-width: 12rem;
  opacity: 95%;
  display: block;
  margin-left: 8rem;
  padding-top: 2rem;
}
p {
  font-size: 1.5rem;
  text-align: center;
};
#app {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
