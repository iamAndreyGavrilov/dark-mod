<script setup>
import { ref } from "vue";
import { useDark, useToggle } from "@vueuse/core";

const isDark = useDark();
const toggleDark = useToggle(isDark);

defineProps({
  msg: String,
});

const count = ref(0);
</script>

<template>
  <h1>{{ msg }}</h1>

  <button type="button" @click="count++">count is: {{ count }}</button>

  <p>isDark: {{ isDark }}</p>
  <button @click="toggleDark()">toggle</button>
</template>

<style scoped>
a {
  color: #42b983;
}
</style>
