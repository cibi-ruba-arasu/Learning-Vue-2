<script setup>
    import { ref } from 'vue';
    let show = ref(true);
</script>

<template>
    <p>V-show : this property does not remove an element from DOM it simply changes the visibilty property in the CSS </p>
    <div class="box" v-show="show"></div>
    <p>The boolean "show" is : {{ show }}</p>
    <button @click="show = !show">Click to change condition</button>
</template>

<style scoped>
    .box{
        background-color: lightsalmon;
        height: 100px;
        width: 100px;
    }
</style>