<template>
  <router-view />
</template>

<script>
import { Dark } from 'quasar'

export default {
  mounted() {
    if (window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches) {
      Dark.set(true)
    } else {
      Dark.set(false)
    }

    // Listen for changes
    window.matchMedia('(prefers-color-scheme: dark)').addEventListener('change', e => {
      Dark.set(e.matches)
    })
  }
}
</script>
