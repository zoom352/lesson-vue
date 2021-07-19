<template>
    <div>sdsd
            <div class="undercard" v-for="(product, index) in products"
            :key="index">
            <Card
              :call="product.call"
              :subscribe="product.suscribe"
              :price="product.price"
              :imgURL="product.imgURL"
              @addToBasket="addToBasket(index)"/>
            </div>
    </div>
</template>


<script>
import Card from './Card.vue'

export default {
    name: "underCard",
    components: {Card},
    data () {
        return {
            products: [
            {
              call: 'trinket Barcelona',
              subscribe: 'incredible affordable',
              price: 'price',
              imgURL: 'https://ic.pics.livejournal.com/dergachev_va/58474394/3464061/3464061_original.jpg'
            },
            {
              call: 'trinket Barcelona',
              subscribe: 'incredible affordable',
              price: 'price',
              imgURL: 'https://ic.pics.livejournal.com/dergachev_va/58474394/3464061/3464061_original.jpg'
            },
            {
              call: 'trinket Barcelona',
              subscribe: 'incredible affordable',
              price: 'price',
              imgURL: 'https://ic.pics.livejournal.com/dergachev_va/58474394/3464061/3464061_original.jpg'
            },
            ]
        }
    },
    methods: {
        addToBasket(index) {
            console.log(index)
        }
    }
}

</script>

<style scoped>

   .undercard {
       display: flex;
   }

</style>




