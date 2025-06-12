<template>
  <router-view />
</template>

<script setup>
import { Dark } from 'quasar'

if (window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches) {
  Dark.set(true)
} else {
  Dark.set(false)
}

// Optional: Listen for changes in preference
window.matchMedia('(prefers-color-scheme: dark)').addEventListener('change', e => {
  Dark.set(e.matches)
})
</script>
