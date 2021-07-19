<template>
    <div class="everythink">
        <div class="carduser">
            <h2>ill learn you</h2>
            <img src="../assets/barcelona.png" width="300px"/>
            <p>quantity of participants: {{users.length}}</p>
            <ul>
                <li
                 v-for="(user, index) in users"
                :key="index">
                {{userFullName(user)}}
                </li>
                <li v-for="(value, key, index) in users[0]"
                :key="index">
                {{ value }}
                </li>
            </ul>
            <p>{{currentPage}}/{{pages}}</p>
            <button
            type="button"
            @click="currentPage--">
                previous
            </button>
            <button v-for="(page) in pages"
            :key="page"
            type="button"
            @click="currentPage = page">{{page}}</button>
            <button
            type="button"
            @click="currentPage++"> 
                next
            </button>
            
        </div>
        <div class="cardwrite">
            <h3>{{getAuthorFullName}}</h3>
            <p>Messi won everythink in this world</p>
            <p>belive me that was egnouth</p>
            <p>its the end</p>
        </div>
    </div>
</template>

<script>

export default {
    name: 'UseCard',
    data() {
        return {
            firstName: 'Leo',
            secondName: 'Karlovich',
            lastName: 'Messi',
            users: [
                {
                    firstName: 'novak',
                    secondName: 'jokovich',
                    lastName: 'novakovich'
                },
                {
                    firstName: 'novak',
                    secondName: 'jokovich',
                    lastName: 'novakovich'
                },
                {
                    firstName: 'novak',
                    secondName: 'jokovich',
                    lastName: 'novakovich'
                },
                {
                    firstName: 'novak',
                    secondName: 'jokovich',
                    lastName: 'novakovich'
                },
            ],
            pages: 3,
            currentPage: 1
        }
    },
    computed: {
        getAuthorFullName() {
            return this.firstName + ' ' + this.secondName + ' ' + this.lastName
        }
    },
    methods: {
        userFullName(user) {
            return user.firstName + ' ' + user.secondName + ' ' + user.lastName
        },
        userExampleName(user) {
            return user.firstName + ' ' + user.secondName + ' ' + user.lastName
        },
        loadUserPage(page) {
            return console.log(page)
        }
    },
    watch: {
        currentPage (page) {
            this.loadUserPage(page)
        }
    }
}
</script>




<style>
.carduser{
   margin-right: 100px;
}
.cardwrite {
    margin-right: 0;
    margin-top: 50px;
}
.everythink {
    display: flex;
    /* margin: -10px; */
}

</style>
