<template>
  <p>Pending: {{ pending }}</p>
  <p>Error: {{ error }}</p>
  <h1>
    Test: {{ data }}
  </h1>
</template>

<script>
export default defineComponent({
  async setup() {
    const test = await useFetch('/api/now', { server: false })
    return { data: test.data, pending: test.pending, error: test.error }
  }
})
</script>
