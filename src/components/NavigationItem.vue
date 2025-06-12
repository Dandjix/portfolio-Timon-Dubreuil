<template>
  <q-timeline-entry>
    <q-item clickable @click="navigate" class="q-pa-sm rounded-borders cursor-pointer" color="primary" v-ripple>
      <q-item-section avatar>
        <q-icon :name="icon" color="primary" />
      </q-item-section>

      <q-item-section>
        <q-item-label class="text-weight-bold">{{ title }}</q-item-label>
        <q-item-label caption>{{ caption }}</q-item-label>
      </q-item-section>
    </q-item>
  </q-timeline-entry>
</template>

<script>
export default {
  name: 'EssentialLink',
  props: {
    title: {
      type: String,
      required: true
    },
    caption: {
      type: String,
      default: ''
    },
    link: {
      type: String,
      default: '#'
    },
    icon: {
      type: String,
      default: ''
    }
  },
  emits: ["navigate"],
  methods: {
    navigate() {
      this.$emit("navigate")
    }
  },
  computed: {
    isExternalLink() {
      return this.link.startsWith('http')
    }
  }
}
</script>
