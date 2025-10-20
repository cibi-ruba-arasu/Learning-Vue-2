<script setup>
    import { ref } from 'vue';
    let show = ref(true);
</script>

<template>
    <p>Conditional Rendering: v-if , v-else-if , v-else</p>
    <div class="box" v-if="show"></div>
    <p>The boolean "show" is : {{ show }}</p>
    <button @click="show = !show">Click to change condition</button>
</template>

<style scoped>
    .box {
        width: 100px;
        height: 100px;
        background-color: lightblue;
    }
</style>