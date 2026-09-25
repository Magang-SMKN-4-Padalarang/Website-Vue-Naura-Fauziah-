<template>
  <div class="min-vh-100 bg-light">

    <!-- Navbar -->
    <nav class="navbar navbar-dark bg-primary shadow">
      <div class="container">

        <span class="navbar-brand fw-bold">
          My Website
        </span>

        <button
          class="btn btn-light"
          @click="logout"
        >
          Logout
        </button>

      </div>
    </nav>


    <!-- Home -->
    <div class="container py-5">

      <div class="card shadow-sm border-0">
        <div class="card-body text-center py-5">

          <h1 class="fw-bold">
            Selamat Datang!
          </h1>

          <p class="text-muted">
            Ini adalah halaman Home.
          </p>

          <button class="btn btn-primary">
            Mulai Sekarang
          </button>

        </div>
      </div>

    </div>

  </div>
</template>


<script>
export default {
  name: "Home",

  methods: {
    logout() {
      this.$emit("logout")
    }
  }
}
</script>
