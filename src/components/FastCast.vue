<template>

<p>
  {{ msg }}
</p>

<!-- v-model assigns value from input to given variable (two-way data binding) -->

  <!-- WAX WEIGHT -->
  <input id="waxWeight" class="wax-weight"  placeholder="Wax Weight"/>
  <br>
  <br>

  <!-- METAL TYPE RADIO GROUP -->
  <section>
      <input name="radio" class="radio" type="radio" id="rRbutton1" value="silver">
      <label for="rButton1">Sterling Silver</label>
      <input name="radio" class="radio" type="radio" id="rButton6" value="bronze">
      <label for="rButton6">Bronze</label>
      <br>
      <input name="radio" class="radio" type="radio" id="rButton2" value="wGold14">
      <label for="rButton2">White Gold 14K</label>
      <input name="radio" class="radio" type="radio" id="rButton3" value="wGold18">
      <label for="rButton3">White Gold 18K</label>
      <br> 
      <input name="radio" class="radio" type="radio" id="rButton4"  value="yGold14">
      <label for="rButton4">Yellow Gold 14K</label>
      <input name="radio" class="radio" type="radio" id="rButton5" value="yGold18">
      <label for="rButton5">Yellow Gold 18K</label>
      <br>
  </section>
  <br>
  
  <!-- BUTTON SIZE -->
  <input id="buttonSize" class="button-size" placeholder="Button Size"/>
  <br>
  <br>

  <!-- @keyup.enter is an event modifier -->
  <button @keyup.enter="calc(metalType, waxWeight, buttonSize)" @click="calc(waxWeight, buttonSize, metalType )">Calculate</button>

            

</template>

<script>

// Defaults exported to DOM
export default {
  // Options Object
  name: 'FastCast',

  // Props are data that will be passed to/from components
  props: {

    msg: String,
    metalType: String,
    specificGravity: Number,
    waxWeight: Number,
    isVisible: Boolean,
    buttonSize: Number,
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
