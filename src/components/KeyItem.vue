<script>
 const onPress = (e) => {
    console.log(e.key)
 }
</script>
<template>
    <span class="wrapper">
        <slot name="val"></slot>
    </span>
</template>
<style scoped>
    .wrapper {
        color: white;
        font-size: 2rem;
        width: 6vw;
        height: 6vw;
        text-align: center;
        border: 1px solid;
        border-radius: 12px;
    }
</style>