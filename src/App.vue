<template>
  <div>
    <button v-if="component != 'ninjas-index'" @click="component = 'ninjas-index'">Show Ninjas</button>
    <button v-if="component != 'dynamic-components'" @click="component = 'dynamic-components'">Show Dynamic Components</button>
    <button v-if="component != 'blog-index'" @click="component = 'blog-index'">Show Blog (input binding)</button>
    <component v-bind:is="component"></component>
  </div>
</template>

<script>

  import DynamicComponents from './components/dynamicComponents/DynamicComponents.vue';
  import NinjasIndex from './components/ninjas/NinjasIndex.vue';
  import blogIndex from './components/InputBinding/blogIndex';

  export default {
    components: {
      'dynamic-components': DynamicComponents,
      'ninjas-index': NinjasIndex,
      'blog-index': blogIndex,
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
    background-color: #f44336; /* Green */
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
