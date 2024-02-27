<script>
import { generate } from 'random-words';
export default {
  props: {
    inputValue: String,
  },
  data: () => {
    displayText: []
  },
  created () {
    this.displayText = [...generate(30).join(' ')].map((item, index) => [index, item]);
    console.log(this.displayText)
    // console.log(this.props)
  },
  updated () {
    // console.log(this.inputValue)
  }
}
</script>
<template>
    <div class="screen">
        <span class="word" v-for="[index, character] in displayText" :class="correct">
          {{ character }}
        </span>
    </div>
</template>
<style scoped>
.screen {
    border: 3px solid hsla(160, 100%, 37%, 1);
    font-size: 2rem;
    text-align: center;
    width: 85vw;
    height: 20vh;
    overflow: hidden;
    padding: 15px 10px;
}
</style>