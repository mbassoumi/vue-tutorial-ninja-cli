<template>
  <div>
    <add-blog></add-blog>
  </div>
</template>

<script>

  import addBlog from './addBlog';

  export default {
    components: {
      'add-blog': addBlog,
    },
    data() {
      return {

      }
    },
    methods: {

    },

  }
</script>

<style scoped>
  body{
    margin: 0;
    font-family: 'sans-serif';
  }
</style>
