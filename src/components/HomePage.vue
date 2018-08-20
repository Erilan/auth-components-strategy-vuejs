<template>
  <div class="PrivatePage">
    <h1>Home Page</h1>
    <router-link :to="{ name: 'PrivatePage'}">Go to the private page</router-link>
  </div>
</template>

<script>
export default {
  name: 'HomePage'
}
</script>

<style scoped>
</style>
