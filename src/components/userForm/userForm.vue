<template>
    <div class="user-form">
        <div class="flex">
            <div class="form-fields">
                <h2>information about myself</h2>
                <div class="form-group"
                     v-for="(fieldValue, fieldLabel, index) in formFields"
                     :key="index">
                     <label :for="fieldLabel">{{fieldLabel}}:</label>
                     <input class="form-control" id="fieldLabel" v-model="formFields[fieldLabel]">
                     </div>
                     <button type="submit" class="btn btn-primary">save</button>
            </div>
            <div class="user-info">
                <h2>watch that</h2>
                <p v-for="(fieldValue, fieldLabel, index) in formFields"
                   :key="index">{{`${fieldLabel}: ${fieldValue}`}}
                   </p>
            </div>
        </div>
        <div class="form-group">
            <label for="additionalField">else area</label>
            <input class="form-control"
                   id="additionalField"
                   v-model="additionalField"
                   />
        </div>
        <button type="button" class="btn btn-success" @click="addNewField">add</button>
    </div>
</template>


<script>

export default {
    name: 'userForm',
    data () {
        return {
            formFields: {
                firstName: '',
                secondName: '',
                lastName: ''
            },
            additionalField: ''
        }
    },

    methods: {
        addNewField() {
            this.$set(this.formFields, this.additionalField, '')
        }
    }
}

</script>

<style scoped>
   .form-group {
       margin-bottom: 20px;
   }
</style>
