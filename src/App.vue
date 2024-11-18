<script setup>
import { ref } from 'vue'
import FavoritePlaces from './components/FavoritePlaces/FavoritePlaces.vue'
import RegistrationForm from './components/Auth/RegistrationForm/RegistrationForm.vue'
import LoginForm from './components/Auth/LoginForm/LoginForm.vue'
import CreateNewPlaceModal from './components/CreateNewPlaceModal/CreateNewPlaceModal.vue'

const isOpen = ref(true)
const closeModal = () => {
  isOpen.value = false
}
const openModal = () => {
  isOpen.value = true
}
</script>

<template>
  <!-- <HomepageView /> -->
  <div class="bg-white h-screen w-[400px]">
    <FavoritePlaces />
    <button @click="openModal" class="text-slate-700">Click me</button>
    <RegistrationForm @submit="console.log" />
    <LoginForm @submit="console.log" />
    <CreateNewPlaceModal :is-open="isOpen" @close="closeModal" @submit="console.log" />
  </div>
</template>
