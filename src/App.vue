<template>
    <div class="container">
        <custom-validations />
    </div>
</template>

<script>
import BasicForm from './components/BasicForm.vue'
import FormValidations from './components/FormValidations.vue'
import ValueBinding from './components/ValueBinding.vue'
import CustomValidations from './components/CustomValidations.vue'
export default {
    name: 'app',
    components: {
        BasicForm,
        FormValidations,
        ValueBinding,
        CustomValidations
    }
};
</script>
