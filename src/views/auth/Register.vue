<template>
    <div class="container">        
        <h3>Register</h3>

        <div class="form-group">
            <label>Full Name</label>
            <input type="text" class="form-control form-control-lg" v-model="user.username">
        </div>

        <div class="form-group">
            <label>Email address</label>
            <input type="email" class="form-control form-control-lg" v-model="user.email">
        </div>

        <div class="form-group">
            <label>Password</label>
            <input type="password" class="form-control form-control-lg" v-model="user.password">
        </div>

        <button class="btn btn-primary btn-lg btn-block" @click="submit">Sign Up</button>

        <p class="forgot-password text-right">
            Already registered 
            <router-link :to="{name: 'Login'}">sign in?</router-link>
        </p>

        <hr>
        <button class="btn btn-secondary" @click="fetchData">Show Data</button>
        <!-- <button class="btn btn-secondary" @click="hideData">Hide Data</button> -->
        <ul class="list-group">
            <li class="list-group-item" v-for="u in users" :key="u.username">{{ u.username }} / {{ u.email }}</li>
        </ul>
        
    </div>
</template>


<script>
export default {
    data(){
        return{
            user: {
                username: '',
                email: '',
                password: ''
            },
            users: []
        }
    },
    methods:{
        submit(){
            console.log(this.user);
            this.$http.post('',this.user)
                .then(response => {
                    console.log(response);
                }, error =>{
                    console.log(error);
                });
        },
        fetchData(){
            this.$http.get('')
                .then(response => {
                    return response.json();                    
                })
                .then(data => {
                    const resultArray = [];
                    for(let key in data){
                        resultArray.push(data[key]);
                    }
                    this.users = resultArray;
                });
            }
        },
        hideData(){
            this.users = [];
        }
    }
</script>

<style scoped>

</style>