<template>
  <h1>Vue11_von_mouseEvent</h1>
  <input type="button" value="" v-on:click="Btn" />
</template>

<script>
export default {
  methods: {
    Btn(e) {
      console.log(e);
      if (e.button === 0) console.log("left");
      else if (e.button === 1) console.log("middle");
      else if (e.button === 2) console.log("right");
    },
  },
};
</script>

<style></style>
