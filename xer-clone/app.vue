<template>
  <div :class="{'dark': darkMode}">
    <h1 class="text-red-500 dark:text-dim-500">Twitter Clone</h1>
  </div>
</template>

<script lang="ts" setup>
  const darkMode = ref(true)
</script>