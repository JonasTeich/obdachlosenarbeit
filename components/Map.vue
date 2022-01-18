<template>
  <Modal v-if="modal.isOpen" @close-modal="closeModal" />
  <GoogleMap
    api-key="AIzaSyAZUHgklFrAiwAfjKxxeOXdBjBoINq6UPA"
    style="width: 100%; height: 600px"
    :center="center"
    :zoom="6"
  >
    <Marker :options="{ position: center }" @click="showModal" />
  </GoogleMap>
</template>

<script>
import { defineComponent } from 'vue'
import { GoogleMap, Marker } from 'vue3-google-map'

export default defineComponent({
  components: { GoogleMap, Marker },
  setup() {
    const center = { lat: 51.1642292, lng: 10.4541194 }
    const modal = reactive({
      isOpen: false
    })

    const showModal = () => {
      modal.isOpen = true
    }

    const closeModal = () => {
      modal.isOpen = false
    }

    return { center, showModal, modal, closeModal }
  },
})
</script>