<template>
  <div>
    <h1>Ninjas list</h1>
    <ul>
      <li v-for="ninja in ninjas">{{ninja}}</li>
    </ul>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        ninjas: ['Majd', 'Basem', 'Bassoumi']
      }
    }
  }
</script>

<style scoped>
  h1{
    color: green;
  }
</style>
