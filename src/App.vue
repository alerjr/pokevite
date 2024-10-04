<script setup>
import { ref } from "vue";

let num = ref(0);
</script>

<template>
  <!-- Navbar -->
  <div>
    <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
      <div class="container-fluid">
        <router-link class="navbar-brand" to="/">
          <img
            src="https://cdn-icons-png.flaticon.com/512/188/188987.png"
            alt="Pokevite"
            width="30"
            height="24"
          />
          PokeVite
        </router-link>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarNav"
          aria-controls="navbarNav"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav">
            <li class="nav-item">
              <router-link class="nav-link" aria-current="page" to="/"
                >Home</router-link
              >
            </li>
            <li class="nav-item">
              <router-link class="nav-link" to="/about">About</router-link>
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <!-- Content -->
    <div class="main">
      <router-view></router-view>
    </div>

    <!-- Footer -->
    <footer class="bg-primary text-light">
      <div>
        Design in
        {{ new Date().getFullYear() }}
      </div>
    </footer>
  </div>
</template>

<style>
body {
  height: 100vh;
  background: rgb(113, 191, 211);
  background: radial-gradient(
    circle,
    rgba(113, 191, 211, 0.7492877492877492) 0%,
    rgba(24, 44, 173, 0.8475783475783476) 100%
  );
}

footer {
  position: fixed;
  bottom: 0;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 50px;
}
</style>