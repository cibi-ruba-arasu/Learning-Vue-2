<script setup>
  import HelloWorld from './components/HelloWorld.vue';
  import Attributes from './components/Attributes.vue';
  import Reactivity from './components/Reactivity.vue';
  import Ref from './components/Ref.vue';
  import Computed from './components/Computed.vue';
  import ConditionalRendering from './components/Conditional-Rendering.vue';
  import VShow from './components/V-show.vue';
</script>

<template>
  <div v-cloak class="app">
    <h1>==== Hello World Component ====</h1>
    <HelloWorld />
    <h1>==== Attributes Component ====</h1>
    <Attributes />
    <h1>==== Reactivity Component ====</h1>
    <Reactivity />
    <h1>==== Ref Component ====</h1>
    <Ref />
    <h1>==== Computed Component ====</h1>
    <Computed />
    <h1>==== Conditional Rendering Component ====</h1>
    <ConditionalRendering />
    <h1>==== V-show Component ====</h1>
    <VShow />
  </div>
</template>

<style scoped>
  [v-cloak] {
    display: none;
  }
  .app{
    background-color:lightgray;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
  }
</style>
