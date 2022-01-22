<template>
  <!-- <Modal v-if="modal.isOpen" @close-modal="closeModal" :selected-location="selectedLocation.data" />
  <GoogleMap
    api-key="AIzaSyAZUHgklFrAiwAfjKxxeOXdBjBoINq6UPA"
    style="width: 100%; height: 600px"
    :center="center"
    :zoom="6"
  >
    <Marker v-for="marker in data" :key="marker.locationName" :options="{ position: marker.position }" @click="showModal(marker.id)" />
  </GoogleMap> -->
</template>

<script>
// import { defineComponent } from 'vue'
// import { GoogleMap, Marker } from 'vue3-google-map'

// export default defineComponent({
//   components: { GoogleMap, Marker },
//   setup() {
//     const center = { lat: 51.1642292, lng: 10.4541194 }

//     const data = [
//       {
//         id: 1,
//         position: { lat: 50.80649287965101, lng: 6.49691765397123 },
//         locationName: 'OVA Düren',
//         responsible: 'Phillipp Freitag',
//         contact: 'freitagphilipp6@gmail.com	'
//       },
//       {
//         id: 2,
//         position: { lat: 50.90231, lng: 7.460005 },
//         locationName: 'Hoffnungsvoll Köln',
//         responsible: 'Derik Ost',
//         contact: 'jonasteichrueb@gmail.com'
//       }
//     ])

//     const modal = reactive({
//       isOpen: false
//     })

//     const selectedLocation = reactive({
//       data: {}
//     })

//     const showModal = (id) => {
//       selectedLocation.data = data.find(element => element.id === id)
//       modal.isOpen = true
//     }

//     const closeModal = () => {
//       modal.isOpen = false
//     }

//     return { center, showModal, modal, closeModal, data, selectedLocation }
//   },
// })
</script>
