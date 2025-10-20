<script setup>
    import { ref } from 'vue';
    const message = ref('Yello World!');
    const add_function =(x,y) => {
        return x + y;
    }
</script>

<template>
    <div>
        <h1>HelloWorld</h1>
        <p>{{ message }}</p>
        <p>{{ add_function(67, 2) }}</p>
    </div>
</template>

<style scoped>

</style>