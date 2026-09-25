<template>
  <div class="container-fluid min-vh-100 d-flex justify-content-center align-items-center bg-light">

    <div class="card shadow p-4" style="width: 400px;">

      <h2 class="text-center mb-2">Login</h2>

      <p class="text-center text-muted mb-4">
        Silakan login 
      </p>

      <form @submit.prevent="login">

        <div class="mb-3">
          <label class="form-label">Username</label>

          <input v-model="username" type="text" class="form-control" placeholder="Masukkan username">
        </div>

        <div class="mb-3">
          <label class="form-label">Password</label>

          <input v-model="password" type="password" class="form-control" placeholder="Masukkan password">
        </div>

        <button type="submit" class="btn btn-primary w-100">
          Login
        </button>

      </form>

      <div v-if="error" class="alert alert-danger mt-3">
        {{ error }}
      </div>

      <div class="text-center text-muted mt-3">
        <small>
          Username: <b>nau</b><br>
          Password: <b>nau123</b></br>
        </small>
      </div>

    </div>


  </div>
</template>

<script>
export default {
  data() {
    return {
      username: "",
      password: "",
      error: ""
    }
  },

  methods: {
    login() {

      if (this.username === "nau" && this.password === "nau123") {
        this.$emit("login-berhasil")
      } else {
        this.error = "Username atau password salah!"
      }
    }
  }
}
</script>
