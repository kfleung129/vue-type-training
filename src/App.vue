<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <div class="wrapper">
    <header>
      <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="50" height="50" />
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/train">Train</RouterLink>
      </nav>
    </header>
    <div class="main">
      <RouterView />
    </div>
  </div>
</template>

<style scoped>
  .wrapper {
    position: absolute;
    top: 30px;
    margin: 0px;
  }
  header {
    display: flex;
    flex-direction: row;
    margin: 0 2rem;
    align-items: center;
  }
  header nav {
    margin-left: 2rem;
  }
  header nav a {
    margin: 0px;
    font-size: 16px;
    font-weight: bold;
    padding: .5rem 1.2rem;
    border-right: 1px solid;
  }
  .main {
    margin-top: 2rem;
  }
</style>
