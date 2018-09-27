<template>
  <form id="app" @submit="checkForm" novalidate="true">

    <p v-if="errors.length">
      <b>Please correct the following error(s):</b>
      <ul>
        <li v-for="(error,index) in errors" :key="index">{{ error }}</li>
      </ul>
    </p>

    <p>
      Given a budget of 100 dollars, indicate how much
      you would spend on the following features for the
      next generation Star Destroyer. Your total must sum up to 100.
    </p>

    <p>
      <input
      v-model.number="weapons"
      type="number"
      name="weapons"
    > Weapons <br/>
      <input
      v-model.number="shields"
      type="number"
      name="shields"
    > Shields <br/>
      <input
      v-model.number="coffee"
      type="number"
      name="coffee"
    > Coffee <br/>
      <input
      v-model.number="ac"
      type="number"
      name="ac"
    > Air Conditioning <br/>
      <input
      v-model.number="mousedroids"
      type="number"
      name="mousedroids"
    > Mouse Droids <br/>
  </p>

      <p>
        Current Total: {{total}}
      </p>

      <p>
        <input
      type="submit"
      value="Submit"
    >
  </p>

  </form>
</template>

<script>
export default {
name : 'CustomValidations2',
data(){
    return {
     errors: [],
    weapons: 0,
    shields: 0,
    coffee: 0,
    ac: 0,
    mousedroids: 0
    }
},
  computed: {
     total: function () {
       // must parse because Vue turns empty value to string
       return Number(this.weapons) +
         Number(this.shields) +
         Number(this.coffee) +
         Number(this.ac+this.mousedroids);
     }
  },
  methods:{
    checkForm: function (e) {
      this.errors = [];

       //if total is not equal to 100
       //display the error the value should be 100
      if (!this.errors.length) {
        return true;
      }

      e.preventDefault();
    }
}
}
</script>

<style>
</style>
