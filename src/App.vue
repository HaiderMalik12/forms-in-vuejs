<template>
    <div class="container">
        <basic-form />
    </div>
</template>

<script>
import BasicForm from './components/BasicForm.vue'
import ValueBindingForm from './components/ValueBinding.vue'
export default {
    name: 'app',
    components: {
        BasicForm,
        ValueBindingForm
    }
};
</script>
