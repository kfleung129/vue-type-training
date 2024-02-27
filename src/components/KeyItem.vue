<script>
export default {
  props: {
    id: String,
    class: String
  },
}
</script>
<template>
    <span class="wrapper" :class=class>
        <slot name="val"></slot>
    </span>
</template>
<style scoped>
    .wrapper {
        color: white;
        font-size: 2rem;
        min-width: 40px;
        width: 6vw;
        min-height: 6vh;
        text-align: center;
        border: 1px solid;
        border-radius: 12px;
        box-shadow: 1px 2px;
    }
    .typed {
        color: hsla(160, 100%, 37%, 1);
        border: 3px solid;
        transition: .1s linear;
    }
</style>