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
  <div>
    <button
      class="px-4 py-2 text-white bg-green-500 rounded dark:bg-purple-500"
      type="button"
      @click="count++"
    >
      count is: {{ count }}
    </button>
  </div>

  <div class="my-5">
    <button
      @click="toggleDark()"
      class="px-4 py-2 text-white bg-green-500 rounded dark:bg-purple-500"
    >
      dark theme
    </button>
  </div>
</template>

<style scoped>
a {
  color: #42b983;
}
</style>
