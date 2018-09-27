<template>
    <div class="container">
        <basic-form />
    </div>
</template>

<script>
import BasicForm from './components/BasicForm.vue'
import FormValidations from './components/FormValidations.vue'
export default {
    name: 'app',
    components: {
        BasicForm,
        FormValidations
    }
};
</script>
