<script setup>
    import { computed, ref } from 'vue';
    let inputValue = ref('');
    let lengthofinput = computed(()=>{
        return inputValue.value.length;
    });
</script>

<template>
    <p>A computed property is used to derive a value based on reactive state.</p>
    <input v-model="inputValue" />
    <p>{{lengthofinput}}/200</p>
</template>

