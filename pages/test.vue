<template>
  <h1>
    Test: {{ data }}
  </h1>
</template>

<script setup>
const data = await $fetch('api/now')
</script>
