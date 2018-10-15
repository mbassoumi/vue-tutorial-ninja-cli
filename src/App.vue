<template>
  <div>
    <keep-alive>
      <component v-bind:is="component"></component>
    </keep-alive>
    <button @click="component = 'form-one'">Show Form One</button>
    <button @click="component='form-two'">Show Form Two</button>
  </div>
</template>

<script>

  import FormOne from './components/FormOne';
  import FormTwo from './components/FormTwo';

  export default {
    components: {
      'form-one': FormOne,
      'form-two': FormTwo,
    },
    data() {
      return {
        component: 'form-one'
      }
    },
    methods: {},

  }
</script>

<style scoped>

</style>
