<script setup>
const router = useRouter()

const loginState = reactive({
  email: ''
})

const checkEmail = () => {
  if (loginState.email === 'jonasteichrueb@gmail.com') {
    router.push('/')
  }
}

useMeta({
  title: 'Herzlich Willkommen!'
})
</script>

<template>
  <div class="h-screen flex justify-center items-center">
    <div class="p-4 bg-gray-200 rounded max-w-lg">
      <h1 class="mb-2 text-xl">Herzlich Willkommen</h1>
      <p class="mb-4 text-gray-900">Um sicherzustellen, dass du zugriff auf die Daten hast, musst du deine E-Mailadresse angeben.</p>
      <div class="flex">
        <input type="email" placeholder="Deine E-Mail" v-model="loginState.email" class="rounded px-2 py-1 w-full" @keypress.enter="checkEmail">
        <button class="bg-gray-400 rounded w-8 h-8 ml-2" @click="checkEmail"><i class="fas fa-arrow-right text-white"></i></button>
      </div>
    </div>
  </div>
</template>
