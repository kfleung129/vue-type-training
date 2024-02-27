<script setup>
import Key from './KeyItem.vue';
const keyboard = [
    ['Q','W','E','R','T','Y','U','I','O','P'],
    ['A','S','D','F','G','H','J','K','L'],
    ['Z','X','C','V','B','N','M']
];
</script>
<script>
export default {
    props: {
        inputValue: String,
    },
    updated () {
        
    }
}
</script>
<template>
    <div class="wrapper">
        <div class="row" v-for="keys in keyboard">
            <Key v-for="key in keys" v-slot:val :id=key :class="{typed: inputValue.toUpperCase()==key}" >
                {{ key }}
            </Key>
        </div>
    </div>
</template>
<style scoped>
.row {
    display: flex;
    flex-direction: row;
    gap: .6rem;
}
.row * {
    margin-top: .5rem;
}
</style>