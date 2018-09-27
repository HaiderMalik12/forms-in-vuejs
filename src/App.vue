<template>
    <div class="container">
        <value-binding />
    </div>
</template>

<script>
import BasicForm from './components/BasicForm.vue'
import FormValidations from './components/FormValidations.vue'
import ValueBinding from './components/ValueBinding.vue'
export default {
    name: 'app',
    components: {
        BasicForm,
        FormValidations,
        ValueBinding
    }
};
</script>
