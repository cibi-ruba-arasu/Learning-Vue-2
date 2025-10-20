<script setup>

    const linkin_park_gif = "https://media2.giphy.com/media/v1.Y2lkPTc5MGI3NjExbTYxams1dWFiZGowMXN2NjFtMDBhMTc1NDFhOHdhOWdhNWR1dDZmbyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/mfhIlzn4UZb68/giphy.gif";

    const width = 300;

</script>

<template>
    <p>Normal GIF</p>
    <img :src="linkin_park_gif" />
    <p>Resized GIF using :style binding</p>
    <img 
        :src="linkin_park_gif" 
        :style="{ width: width + 'px' }" 
    />
    <p>Redirection using anchor tags</p>
    <a
        :href="'https://www.linkinpark.com/'" 
        target="_blank" 
        rel="noopener"
    >Linkin Park website</a>
</template>

<style scoped>

</style>