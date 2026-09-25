<template>
  <Login
    v-if="!isLogin"
    @login-berhasil="isLogin = true"
  />

  <Home
    v-else
    @logout="isLogin = false"
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
      isLogin: false
    }
  }
}
</script>