<template>
  <div id="app">
    <MyComponent/>
    <TrainButton/>
    <UseCard/>
    <PhotoRedactor/>
    <PropsEmitVmodel/>
    <underCard/>
    <userForm/>
    <Validations/>
  </div>
</template>

<script>
// import MyComponent from './components/MyComponent.vue'
// import TrainButton from './components/TrainButton.vue'
// import UseCard from './components/UseCard.vue'
// import PhotoRedactor from './components/VifVshow.vue'
// import PropsEmitVmodel from './components/PropsEmitVmodel.vue'
// import underCard from './components/lesson2/underCard.vue'
// import userForm from './components/userForm/userForm.vue'
import Validations from './components/Validations/Validations.vue'

export default {
  name: 'App',
  components: {
    Validations,
    // userForm,
    // underCard,
    // PropsEmitVmodel
    // PhotoRedactor
    // MyComponent,
    // TrainButton,
    // UseCard
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
