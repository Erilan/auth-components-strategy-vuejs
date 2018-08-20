<template>
  <div class="TheLogin">
    <h1>Login</h1>

    <div>
      <input type="text" name="username" placeholder="Username">
      <br>
      <input type="password" name="password" placeholder="Password">
      <br><br>
      <button @click="logIn">Log in</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TheLogin',
  methods: {
    logIn() {
      this.$emit('TheLogin::loginResult', {loginResult: true})
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  margin: 40px 0 0;
  color: blue;
}

</style>
