<script setup>
import {ref} from 'vue'
</script>

<template>
  <nav class="navbar bg-white text-light" data-bs-theme="light">
    <div class="container">
      <ul class="nav">
        <li class="nav-item">
          <router-link class="navbar-brand" to="/">Rick and Morty</router-link>
        </li>
        <li class="nav">
          <router-link class="nav-link" aria-current="page" to="/">Início</router-link>
        </li>
        <li class="nav">
          <router-link class="nav-link" to="/about">Sobre</router-link>
        </li>
      </ul>
    </div>
  </nav>
  
  <div class="main">
    <router-view></router-view>
  </div>

  <footer class="bg-white text-dark">
    <div>
      Unimar | ADS | {{ new Date().getFullYear() }}
    </div>
  </footer>
</template>
<style>
footer{
  position: fixed;
  bottom: 0;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 40px;
}
</style>


