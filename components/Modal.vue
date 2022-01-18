<script>
import { defineComponent } from 'vue'

export default defineComponent({
  methods: {
    closeModal () {
      this.$emit('closeModal')
    }
  }
})
</script>



<template>
  <div class="fixed top-0 left-0 w-full h-full bg-gray-900 bg-opacity-70 z-50 flex justify-center items-center">
    <div class="relative bg-white opacity-100 p-4 rounded max-w-lg w-full">
      <div class="absolute rounded-full bg-gray-400 h-6 w-6 cross flex justify-center items-center cursor-pointer" @click="closeModal">
        <i class="fas fa-times text-white"></i>
      </div>
      <h1>Düren</h1>
    </div>
  </div>
</template>

<style scoped>
.cross {
  right: -10px;
  top: -10px;
}
</style>
