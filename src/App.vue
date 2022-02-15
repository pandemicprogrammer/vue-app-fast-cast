<template>
  <div id="app">
    <div class="container">
      <img src="./assets/logo.png" alt="logo" class="logo">

       <br>
      <input
      id="waxWeight"
      class="wax-weight"
      v-model.number="waxWeight"
      placeholder="Wax Weight"
    />
    <br/>
      <br />
    <input
      name="radio"
      class="radio"
      type="radio"
      id="rRbutton"
      v-model.number="specificGravity"
      value="11.5"
    />
    <label for="rButton1">Bronze</label>
    <br>    <br/>

    <input
      name="radio"
      class="radio"
      type="radio"
      id="rRbutton"
      v-model.number="specificGravity"
      value="10.3"
    />
    <label for="rButton1">Sterling Silver</label>
    <br />    <br/>

     <input
      name="radio"
      class="radio"
      type="radio"
      id="rRbutton"
      v-model.number="specificGravity"
      value="11.5"
    />
    <label for="rButton1">White Gold 14K</label>

     <br>    <br/>

     <input
      name="radio"
      class="radio"
      type="radio"
      id="rRbutton"
      v-model.number="specificGravity"
      value="11.5"
    />
    <label for="rButton1">White Gold 18K</label>

    <br>    <br/>

     <input
      name="radio"
      class="radio"
      type="radio"
      id="rRbutton"
      v-model.number="specificGravity"
      value="11.5"
    />
    <label for="rButton1">Yellow Gold 14K</label>

     <br>    <br/>
     <input
      name="radio"
      class="radio"
      type="radio"
      id="rRbutton"
      v-model.number="specificGravity"
      value="11.5"
    />
    <label for="rButton1">Yellow Gold 18K</label>
    
    
    <br> <br>
    <input
      id="buttonSize"
      class="button-size"
      v-model.number="buttonSize"
      placeholder="Button Size"
    />       
    <br> 
    <label >Button Size</label>
    <br>

    
  <br> <br>
  <button @click="calculateMetalWeight">Calculate</button>
    <p>{{ metalWeight.toFixed(2) }} gm</p>

    </div>
    
  </div>
</template>

<script>
export default {
  name: "App",

  methods: {
    calculateMetalWeight() {
      this.metalWeight =
        (this.waxWeight + this.waxWeight * this.buttonSize) *
        this.specificGravity;
    },
  },

  // DATA
  data() {
    return {
      waxWeight: "",
      metalType: "",
      buttonSize: 0.1,
      metalWeight: "",
      specificGravity: "",
    };
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
