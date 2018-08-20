<template>
  <div id="app">
    <router-view v-if="isLoggedIn"></router-view>
    <TheLogin v-else @TheLogin::loginResult="handleLoginResult"/>
  </div>
</template>

<script>
import TheLogin from './components/TheLogin'

export default {
  name: 'app',
  components: {
    TheLogin
  },
  data() {
    return {
      userIsLoggedIn: false
    }
  },
  computed: {
    isLoggedIn() {
      return this.userIsLoggedIn
    }
  },
  methods: {
    handleLoginResult({loginResult}) {
      this.userIsLoggedIn = loginResult
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
