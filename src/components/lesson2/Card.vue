<template>
    <div>
        <div class="card">
            <img :src="imgURL" width="200px"/>
            <h4>{{call}}</h4>
            <p>{{subscribe}}</p>
            <p>{{price}}: 200</p>
            <button type="button" @click="addToBasket()">add it in the bascet</button>
        </div>
    </div>
</template>


<script>


export default {
    name: 'Card',
    props: {
      call: {
          type: String,
          validator(value) {
              return value.length < 20
          }
      }, 
      subscribe: {
          type: String,
          default: 'nothing'
      }, 
      price: {
          type: Number,
          default: 0 
      }, 
      imgURL: {
          type: String,
          default: 'nothing'
      }
    },
    methods: {
        addToBasket() {
            this.$emit('addToBasket')
        }
    }
    // data () {
    //     return {
    //         call: 'trinket Barcelona',
    //         subscribe: 'incredible affordable',
    //         price: 'price',
    //         imgURL: 'https://ic.pics.livejournal.com/dergachev_va/58474394/3464061/3464061_original.jpg'
    //     }
    // }
}

</script>

<style scoped>

.image {
    margin-right: 200px;
}

.card {
    border: solid 2px black;
    width: 200px;
    height: 300px;
}

</style>