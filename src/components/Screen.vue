<script>
import { generate } from 'random-words';
export default {
  props: {
    inputValue: String,
  },
  setup(props) {
    console.log(props.inputValue)
  },
  data: () => {
    displayText: []
  },
  created () {
    this.displayText = [...generate(30).join(' ')];
    console.log(this.displayText)
    console.log(this.props)
  },
}
</script>
<template>
    <div class="screen">
        {{ displayText.join('') }}
        {{ inputValue }}
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