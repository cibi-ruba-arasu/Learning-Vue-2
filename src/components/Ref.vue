<script setup>
    import { ref } from 'vue';
    let count = ref(0);
</script>

<template>
    <p>Ref() Function is only used in cases where you need to create a reactive reference to a primitive value.</p>
    <p>Count: {{ count }}</p>
    <button @click="count++">Increment Count</button>
    <button @click="count--">Decrement Count</button>
</template>

<style scoped>

</style>