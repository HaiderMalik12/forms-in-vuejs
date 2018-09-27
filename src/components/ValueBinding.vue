<template>
    <div class="form-group">
        <select v-model="selected" class="form-control">
            <!-- use v-for for the options -->
        </select>
        <p>Selected: {{ selected }}</p>

        <input type="number" class="form-control">
        <p> Age : {{age}} </p>

        <input type="text" class="form-control"/>
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
