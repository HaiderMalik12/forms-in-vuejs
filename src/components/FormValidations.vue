<template>
    <form @submit="checkForm">
        <div class="form-group col-4">
            <label for="name">Name</label>
            <input class="form-control" id="name" v-model="name" type="text" name="name"/>
        </div>
            <div class="form-group col-4">
                <label for="age">Age</label>
                <input class="form-control" id="age" v-model="age" type="number" name="age" min="0"/>
              </div>
                <div class="form-group col-4">
                    <label for="tickets">Tickets </label>
                    <input class="form-control" id="tickets" v-model="tickets" type="number" name="tickets" min="0"/>
              </div>
                    <div class="form-group col-4">
                        <label for="movie">Select Movie</label>
                        <select id="movie" v-model="movie" name="movie" class="form-control">
                            <option>Star Wars</option>
                            <option>Vanilla Sky</option>
                            <option>Atomic Blonde</option>
                        </select>
                    </div>
                    <div class="form-group col-4">
                        <input class="btn btn-primary" type="submit" value="Submit"/>
                </div>
    </form>
</template>

<script>
export default {
 name: 'FormValidations',
 data(){
     return {
       errors: [],
       name: null,
       age: null,
       movie: null,
       tickets: null
     }
 },
 methods:{
     checkForm: function (e) {
      e.preventDefault();

      //Add validations for required attributes

      //if there is no error then return the true

    }
 }
}
</script>

<style>
</style>
