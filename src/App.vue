<template>
  <Login
    v-if="!isLogin"
    @login-berhasil="loginBerhasil"
  />

  <Home
    v-else
    @logout="logout"
  />
</template>

<script>
import Login from "./views/login.vue"
import Home from "./views/home.vue"

export default {
  components: {
    Login,
    Home
  },

  data() {
    return {
      isLogin: localStorage.getItem("isLogin") === "true"
    }
  },

  methods: {
    loginBerhasil() {
      this.isLogin = true
      localStorage.setItem("isLogin", "true")
    },

  logout() {
    this.isLogin = false
    localStorage.removeItem("isLogin")
  }
  }
}
</script>