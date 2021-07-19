<template>
    <div>
            <button
            type="button"
            @click="increase">increase</button>

            <input 
            type="number" 
            :value="count"
            :min="minCount"
            :max="maxCount"/>

            <button 
            type="button"
            @click="decreace">decrease</button>
    </div>
</template>


<script>

export default {
    name: 'TrainButton',
    data() {
        return {
            count: 1,
            maxCount: 10,
            minCount: 1
        }
    },
    methods: {
    increase() {
        if(this.count < this.maxCount) {
            this.count++
        }
    },
    decreace() {
        if (this.count > this.minCount) {
            this.count--
        }
    }
    }


}
</script>
