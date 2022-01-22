<script>
import { defineComponent } from 'vue'

export default defineComponent({
  props: {
    selectedLocation: Object
  },
  methods: {
    closeModal () {
      this.$emit('closeModal')
    }
  }
})
</script>



<template>
  <div class="fixed top-0 left-0 w-full h-full bg-gray-900 bg-opacity-40 z-50 flex justify-center items-center p-4">
    <div class="relative bg-white opacity-100 p-4 rounded max-w-lg w-full">
      <div class="absolute rounded-full bg-red-400 h-6 w-6 cross flex justify-center items-center cursor-pointer" @click="closeModal">
        <i class="fas fa-times text-white"></i>
      </div>
      <h1 class="text-2xl mb-4">{{ selectedLocation.locationName }}</h1>
      <div class="flex flex-col">
        <span>Verantwortliche(r): {{ selectedLocation.responsible }}</span>
        <span>
          E-Mail: 
          <a :href="'mailto:' + selectedLocation.contact" class="text-gray-700 underline">
            {{ selectedLocation.contact }}
          </a>
        </span>
      </div>
    </div>
  </div>
</template>

<style scoped>
.cross {
  right: -8px;
  top: -8px;
}
</style>
