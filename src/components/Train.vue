<script setup>
import Keyboard from './Keyboard.vue';
import Screen from './Screen.vue';
</script>
<script>
export default {
  data: () => ({
    inputValue: ""
  }),
  methods: {
    onType: function(e) {
      this.inputValue = e.target.value.replace(/[^a-zA-Z]+/g, '');
      console.log(this.inputValue);
    },
  },
  mounted () {
    this.$nextTick(() => this.$refs.userInput.focus())
  }
}
</script>
<template>
  <div class="wrapper">
    <Screen :inputValue=inputValue />
    <input ref="userInput" @blur="$refs.userInput.focus()" @input="onType">
    <Keyboard :inputValue=inputValue.slice(-1) />
  </div>
</template>

<style scoped>
.wrapper {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-top: 5rem;
  width: 100vw;
}

.screen {
  border: 3px solid hsla(160, 100%, 37%, 1);
  font-size: 2rem;
  text-align: center;
  width: 85vw;
  height: 20vh;
  overflow: hidden;
  padding: 15px 10px;
}

input {
  background-color: transparent;
  color: white;
  margin-top: 1rem;
}
</style>
