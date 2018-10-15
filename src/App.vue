<template>
  <div>
    <component v-bind:is="component"></component>
    <button v-if="component != 'ninjas-index'" @click="component = 'ninjas-index'">Show Ninjas</button>
    <button v-if="component != 'dynamic-components'" @click="component = 'dynamic-components'">Show Dynamic Components</button>
  </div>
</template>

<script>

  import DynamicComponents from './components/dynamicComponents/DynamicComponents.vue';
  import NinjasIndex from './components/ninjas/NinjasIndex.vue';

  export default {
    components: {
      'dynamic-components': DynamicComponents,
      'ninjas-index': NinjasIndex,
    },
    data() {
      return {
        component: 'ninjas-index'
      }
    },
    methods: {},

  }
</script>

<style scoped>
  button {
    background-color: #4CAF50; /* Green */
    border: none;
    color: white;
    padding: 15px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
  }
</style>
