<template>
  <div id="app" class="app">  
    <div class="container">
      <img src="./assets/logo.png" alt="logo" class="logo">

          <p>{{ parseFloat(metalWeight).toFixed(2) }} grams</p>
          <p>{{ parseFloat(pennyWeight).toFixed(2) }} pennyweight</p>

       <button @click="calculateMetalWeight">Calculate</button>

      <br> <br>

      <input
      id="waxWeight"
      class="wax-weight"
      v-model.number="waxWeight"
      placeholder="0.00 Wax Weight"
    />
    <br>     <br>

    <input
      id="buttonSize"
      class="button-size"
      v-model.number="buttonSize"
      placeholder="0.00 Button Size"
    />    
      <br /> <br>
   
   <input
      name="radio"
      class="radio"
      type="radio"
      id="rRbutton"
      v-model.number="specificGravity"
      value="8.8"
    />
    <label for="rButton1">Bronze</label>
    <br>    <br/>

    <input
      name="radio"
      class="radio"
      type="radio"
      id="rRbutton"
      v-model.number="specificGravity"
      value="10.4"
    />
    <label for="rButton1">Sterling Silver</label>
    <br />    <br/>

     <input
      name="radio"
      class="radio"
      type="radio"
      id="rRbutton"
      v-model.number="specificGravity"
      value="13.7"
    />
    <label for="rButton1">White Gold 14K</label>

     <br>    <br/>

     <input
      name="radio"
      class="radio"
      type="radio"
      id="rRbutton"
      v-model.number="specificGravity"
      value="15.7"
    />
    <label for="rButton1">White Gold 18K</label>

    <br>    <br/>

     <input
      name="radio"
      class="radio"
      type="radio"
      id="rRbutton"
      v-model.number="specificGravity"
      value="13.4"
    />
    <label for="rButton1">Yellow Gold 14K</label>

     <br>    <br/>
     <input
      name="radio"
      class="radio"
      type="radio"
      id="rRbutton"
      v-model.number="specificGravity"
      value="15.5"
    />
    <label for="rButton1">Yellow Gold 18K</label>
    
    
    <br> <br>


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

        this.pennyWeight = this.metalWeight * 0.643015;
    },
  },

  // DATA
  data() {
    return {
      specificGravity: "",
      buttonSize: 0.1,
      metalWeight: "",  
      waxWeight: "",
      pennyWeight: ""
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

<style>
@font-face {
  font-family: "Patrick";
  src: local("Patrick"),
   url(./assets/fonts/PatrickHandSC-Regular.ttf) format("truetype");
}
</style>
