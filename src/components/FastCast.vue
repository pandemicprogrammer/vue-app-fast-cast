// COMPONENT TEMPLATE

<template>
<div class="container">

  <!-- v-model assigns value from input to given variable (two-way data binding) -->
  <input class="input" type="text" placeholder="Wax Weight" v-model="waxWeight">
  <br><br>

  <!-- METAL TYPE RADIO GROUP -->
  <section>
    <input name="radio" class="radio" type="radio" id="rButton6" v-model="bronze">
    <label for="rButton6">Bronze</label>
    <br> <br>
    <input name="radio" class="radio" type="radio" id="rRbutton1" v-model="silver">
    <label for="rButton1">Sterling Silver</label>
    <br> <br>
    <input name="radio" class="radio" type="radio" id="rButton2" vmodel="wGold14">
    <label for="rButton2">White Gold 14K</label>
    <br> <br>
    <input name="radio" class="radio" type="radio" id="rButton3" vmodel="wGold18">
    <label for="rButton3">White Gold 18K</label>
    <br> <br>
    <input name="radio" class="radio" type="radio" id="rButton4"  vmodel="yGold14">
    <label for="rButton4">Yellow Gold 14K</label>
    <br> <br>
    <input name="radio" class="radio" type="radio" id="rButton5" vmodel="yGold18">
    <label for="rButton5">Yellow Gold 18K</label>
    <br>
  </section>
  <br>
  
  <!-- BUTTON SIZE -->
  <input id="buttonSize" class="input" type="text" placeholder="Button (Default .10)" v-model="buttonSize">

  <br>
  <br>

  <!-- @keyup.enter is an event modifier -->
  <button @keyup.enter="calc(metalType, waxWeight, buttonSize)" @click="calc(waxWeight, buttonSize, metalType )">Calculate</button>
  <img class="logo" src="src/assets/logo.png" alt="logo">
</div>

  
            

</template>

<script>

// Defaults exported to DOM
export default {

  buttonSize: .1,  

  // Options Object
  name: 'FastCast',

  // Props are data that will be passed to/from components
 
}

alert('test')
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container {
  padding: 1rem;
  text-align: center;
  border: solid gray;
  border-radius: .5rem;
  }
</style>
