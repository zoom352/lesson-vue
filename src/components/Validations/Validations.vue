<template>
    <div>
        <div>
            <p>Login</p>
            <input 
               type="Login" v-model="Login"/>
        </div>
        <div>
            <p>Email</p>
            <input
               type="Email" v-model="Email"/>
        </div>
        <div>
            <p>Password</p>
            <input 
                 type="Password" v-model="Password"/>
        </div>
        <br/>
        <div class="form-group">
            <label for="country"></label>
            <select id="country" v-model="country2">
                <option v-for="(country, index) in countrys"
            :key="index">{{country.label}}</option>
            </select>
        </div>
    </div>
</template>

<script>

export default {
    name: 'Validations',
    data () {
        return {
            Login: '',
            Email: '',
            Password: '',
            country2: '',
            countrys: [
                {label: 'Украина',
                 value: 'Ukraine'},
                 {label: 'Канада',
                 value: 'Canada'},
                 {label: 'США',
                 value: 'USA'}
            ]
        }
    }
}

</script>
