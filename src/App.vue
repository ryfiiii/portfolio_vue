<template>
  <div>
    <transition name="fade">
      <LoadingAnimation v-if="isLoading" />
    </transition>
      <div v-if="!isLoading">
        <Header />
        <Home />
        <Footer />
      </div>
  </div>
</template>

<script setup lang="ts">
import LoadingAnimation from "@/components/LoadingAnimation.vue"
import Header from "@/components/Header.vue"
import Home from "@/views/Home.vue"
import Footer from "@/components/Footer.vue"
import { onMounted, ref } from "vue"

const isLoading = ref<boolean>(false)

onMounted(() => {
  if (!sessionStorage.getItem("isFirstLoad")) {
    isLoading.value = true
    sessionStorage.setItem("isFirstLoad", "true")
    console.log("sessionStorage Set!")

    setTimeout(() => {
      isLoading.value = false
    }, 1300)
  }
})

const deleteSessionStorage = () => {
  if (sessionStorage.getItem("isFirstLoad")) {
    sessionStorage.removeItem("isFirstLoad")
  }
}
</script>

<style scoped>
.fade-enter-active, .fade-leave-active {
   will-change: opacity;
   transition: opacity 0.75s;
}

.fade-enter, .fade-leave-to {
   opacity: 0
}
</style>