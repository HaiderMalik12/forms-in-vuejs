<template>
    <form @submit="checkForm">
        <div class="form-group">
            <p v-if="errors.length">You have to correct these followinge errors:</p>
            <ul>
                <li class="text-danger" v-for="(error, index) in errors" :key="index"> {{error}}</li>
            </ul>
        </div>
        <div class="form-group col-4">
            <label for="name">Name</label>
            <input class="form-control" id="name" v-model="name" type="text" name="name"/>
        </div>
            <div class="form-group col-4">
                <label for="email">Email</label>
                <input class="form-control" id="email" v-model="email" type="email" name="email"/>
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
       tickets: null,
       email: null
     }
 },
 methods:{
     checkForm: function (e) {
      e.preventDefault();

     this.errors = []
      //Add validations for required attributes
      if(!this.name){
          this.errors.push('Name required');
      }
       if(!this.age){
          this.errors.push('Age required');
      }
       if(!this.movie){
          this.errors.push('Movie required');
      }
       if(!this.tickets){
          this.errors.push('Tickets required');
      }
      //if there is no error then return the true
      if(!this.errors.length){
          return true;
      }

    },
    validEmail: function (email) {
      var re = /^(([^<>()\[\]\\.,;:\s@"]+(\.[^<>()\[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
      return re.test(email);
    }
 }
}
</script>

<style>
</style>
