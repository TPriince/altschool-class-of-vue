<template>
  <h1>Color Picker Game</h1>

  <div>{{ message }}</div>

  <button v-for="color in colors" :key="color" @click="matchColor(color)">
    {{ color }}
  </button>
</template>

<script setup>
import { useMathColor } from "../composables/useMathColor.js";
const colors = ["green", "red", "blue", "purple"];

const { message, matchColor } = useMathColor(colors);

</script>

<style></style>
