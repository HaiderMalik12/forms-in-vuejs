<template>
    <div>
        <form>
            <div class="form-group">
                <label for="exampleInputEmail1">Email address</label>
                <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="Enter email" />
            </div>
                <div class="form-group">
                    <label for="exampleInputPassword1">Password</label>
                    <input type="password" class="form-control" id="exampleInputPassword1" placeholder="Password" >
            </div>
                    <div class="form-group">
                        <label for="address">Address</label>
                        <textarea v-model="address" class="form-control" id="address">
            </textarea>
                    </div>
                    <div class="form-group form-check">
                        <input type="checkbox" class="form-check-input" id="exampleCheck1" >
                        <label class="form-check-label" for="exampleCheck1">Check me out</label>
                    </div>

                    <!-- Multiple checkboxes -->

                    <div class="form-group">
                        <input type="checkbox"  id="exampleCheck2" />
                        <label class="form-check-label" for="exampleCheck2">Frontend conference</label>
                        <input type="checkbox"  id="exampleCheck3"/>
                        <label class="form-check-label" for="exampleCheck2">Backend conference</label>
                    </div>

                    <!-- Radio Button -->
                    <div class="form-check">
                        <input class="form-check-input" type="radio" name="exampleRadios" id="exampleRadios1"  checked >
                        <label class="form-check-label" for="exampleRadios1">
                            Male
                        </label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" name="exampleRadios" id="exampleRadios2"/>
                        <label class="form-check-label" for="exampleRadios2">
                            Female
                        </label>
                    </div>
                    <!-- Select Boxes -->
                    <div class="form-group">
                        <label for="inputState">Location</label>
                        <select id="inputState" class="form-control">
                            <option selected>Choose...</option>
                            <option>UK</option>
                            <option>USA</option>
                            <option>Canada</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label for="inputState">Sessions</label>
                        <select id="inputState" class="form-control" multiple>
                            <option>S1</option>
                            <option>S2</option>
                            <option>S3</option>
                        </select>
                    </div>

                    <button type="submit" class="btn btn-primary">Submit</button>
        </form>
        <hr/>
        <p>Email {{email}}</p>
        <p>Passowrd {{password}}</p>
        <p>Address {{address}}</p>
        <p>Checked {{checked}}</p>
        <p>Checked names: {{ conferenceNames }}</p>
        <p>Gender: {{gender}}</p>
        <p>Location: {{location}}</p>
        <p>Sessions: {{sessions}}</p>
    </div>
</template>
<script>
export default {
    name: 'UserForm',
    methods:{
        submit(e){
         e.preventDefault()
        }
    }
}
</script>
