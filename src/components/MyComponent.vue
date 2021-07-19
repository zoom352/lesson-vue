<template>
    <div>
        <label>
            add email
            <input type="email" v-bind:value="email" @input="emailInput"/>
        </label>
        <label>
            add password
            <input type="password" v-bind:value="password" v-on:input="emailInput"/>
        </label>
    </div>
</template>

<script>

export default {
    name: 'MyComponent',
    data () {
        return {
            email: 'dimakul.spb@inbox.ru',
            password: '1234'
        }
    },
    methods: {
        emailInput(event) {
            console.log(event.target.value)
        }
    }
}
</script>

