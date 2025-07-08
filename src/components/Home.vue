<template>

<!--===============
동영상
=================-->
<div class="home-video">
  <video autoplay
  src="@/assets/img/video.mp4"
  playsinline
  muted
  ></video>
</div>

<Theme/>
<Slide/>
<Works/>

</template>


<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue'
import Theme from '@/components/home/Theme.vue'
import Slide from '@/components/home/Homeslide.vue'
import Works from '@/components/home/Works.vue'
</script>