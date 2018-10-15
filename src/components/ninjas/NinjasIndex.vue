<template>
  <div>
    <app-header v-bind:title="title" v-on:changeTitle="updateTitle($event)"> </app-header>
    <ninjas v-bind:ninjas="ninjas"></ninjas>
    <app-footer v-bind:title="title"></app-footer>
  </div>
</template>

<script>
  import Header from './Header'
  import Footer from './Footer'
  import Ninjas from './Ninjas'

  export default {
    components: {
      'app-header': Header,
      'app-footer': Footer,
      'ninjas': Ninjas,
    },
    data() {
      return {
        ninjas: [
          {name: 'Ryu', speciality: 'Vue Components', show: false},
          {name: 'Crystal', speciality: 'HTML Wizardry', show: false},
          {name: 'Hitoshi', speciality: 'Click Events', show: false},
          {name: 'Tango', speciality: 'Conditionals', show: false},
          {name: 'Kami', speciality: 'Webpack', show: false},
          {name: 'Yoshi', speciality: 'Data Diggin', show: false}
        ],
        title: 'Vue Ninja Title',
      }
    },
    methods:{
      updateTitle(updatedTitle){
        this.title = updatedTitle;
      }
    }
  }
</script>

<style scoped>
  h1{
    color: purple;
  }
</style>
