<template>
  <h1>v-if</h1>
  <div v-if="x > 23">e{{ x }}</div>
  <div v-else>g{{ x }}</div>
</template>

<script>
export default {
  data() {
    return { x: Math.floor(Math.random() * 45) + 1 };
  },
};
</script>

<style></style>
