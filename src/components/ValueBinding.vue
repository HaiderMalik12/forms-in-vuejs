<template>
    <div class="form-group">
        <select v-model="selected" class="form-control">
            <!-- use v-for for the options -->
            <option v-for="(option, index) in options" :key="index" :value="option.value">{{option.text}}</option>
        </select>
        <p>Selected: {{ selected }}</p>

        <!-- Add number modifier -->
        <input v-model.number ="age" type="number" class="form-control">
        <p> Age : {{age}} </p>

        <!-- add trim message modifier -->
        <input v-model.trim ="msg" type="text" class="form-control"/>
        <p>Message: {{msg}} </p>
    </div>
</template>

<script>
export default {
name: 'ValueBindingForm',
data(){
    return {
    selected: 'A',
    age: '',
    msg: '',
    options: [
      { text: 'One', value: 'A' },
      { text: 'Two', value: 'B' },
      { text: 'Three', value: 'C' },
      { text: 'Four', value: 'D' },
    ]
  }
}
}
</script>

<style>
</style>
