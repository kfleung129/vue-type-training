<script setup>
import { RouterLink } from 'vue-router'
</script>

<template>
  <div class="wrapper">
    <div class="greetings">
      <img alt="Vue logo" class="logo" src="@/assets/keyboard.png" width="auto" height="350px" />
      <h3>
        "Transform Your Typing Skills with Our Comprehensive Type Training Program: Boost Speed, Accuracy, and Efficiency for Success in the Digital World!"
      </h3>
    </div>
    <button @click="$router.push('/train')">Try it!</button>
  </div>
</template>

<style scoped>
.wrapper {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 100vw;
}

h3 {
  font-size: 1.4rem;
  width: 400px;
}

.greetings {
  width: 100%;
  margin-top: 5rem;
  display: flex;
  justify-content: center;
  align-items: center;
}

.greetings * {
  margin-right: 20px;
}

.wrapper button {
  background-color: transparent;
  border: 1px solid;
  border-radius: 12px;
  padding: .5rem 1.8rem;
  font-size: 30px;
  color: hsla(160, 100%, 37%, 1);
  width: fit-content;
}

button:hover {
  background-color: hsla(160, 100%, 37%, 0.2);
  transition: .5s;
  cursor: pointer;
}
</style>
