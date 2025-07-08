<template>
    <v-btn icon
    v-if="showScrollBtn"
    @click="scrollToTop"
    variant="text"
    :style="`--bottom-offset: ${scrollBottomOffset}px`"
    class="scroll-top d-flex justify-center align-center">
    <div class="d-flex flex-column align-center">
        <v-icon>mdi-chevron-up</v-icon>
        <p class="date">TOP</p>
    </div>
    </v-btn>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const showScrollBtn = ref(false)

const handleScroll = () => {
  showScrollBtn.value = window.scrollY > 200
}

const scrollToTop = () => {
  window.scrollTo({ top: 0, behavior: 'smooth' })
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>