<template>
    <div class="col-6 mx-auto">
        <h1>Edit materi</h1>
        <b-form @submit="onSubmit" @reset="onReset">
        <b-form-group
            id="input-group-1"
            label="Email address:"
            label-for="input-1"
            description="We'll never share your email with anyone else."
        >
            <b-form-input
            id="input-1"
            v-model="form.email"
            type="email"
            required
            placeholder="Enter email"
            ></b-form-input>
        </b-form-group>

        <b-form-group id="input-group-2" label="Your Name:" label-for="input-2">
            <b-form-input
            id="input-2"
            v-model="form.name"
            required
            placeholder="Enter name"
            ></b-form-input>
        </b-form-group>

        <!-- <b-form-group id="input-group-3" label="Food:" label-for="input-3">
            <b-form-select
            id="input-3"
            v-model="form.food"
            :options="foods"
            required
            ></b-form-select>
        </b-form-group> -->


        <b-button type="submit" variant="primary">Submit</b-button>
        <b-button type="reset" variant="danger">Reset</b-button>
        </b-form>
    </div>
</template>

<script>
import { isNullOrUndefined } from 'util'
export default {
    data(){
        return {
            form:{
                name:'',
                email:''
            }
        }
    },
    created() {
        console.log(isNullOrUndefined(this.$route.params.id))
        if (isNullOrUndefined(this.$route.params.id)){
           // this.form.name = this.$route.params.mapel
            console.log('undifined item coeg')
        }
    },
    methods:{
        onSubmit(){},
        onReset(){}
    }
}
</script>