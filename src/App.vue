<script setup>
import { onMounted } from 'vue'
import { RouterView } from 'vue-router'
import Nav from '@/components/Nav.vue'

onMounted(() => {
  const tidioScript = document.createElement('script')
  tidioScript.src = '//code.tidio.co/fixhadwpcbt1ewuryyzlbpydljcxxymb.js'
  tidioScript.async = true
  document.body.appendChild(tidioScript)
})
</script>

<template>
  <Nav />
  <RouterView />
</template>
