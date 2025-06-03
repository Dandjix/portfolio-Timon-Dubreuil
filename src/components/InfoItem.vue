<template>
  <q-item clickable>

    {{ value }}

    <q-item-section avatar @click="copyToClipboard">
      <q-icon :name="icon" />
    </q-item-section>
  </q-item>
</template>

<script>
export default {
  props: {
    icon: String,
    value: String,
    copiedValue: String,
    name: String,
  },
  methods: {
    copyToClipboard() {
      navigator.clipboard.writeText(this.copiedValue).then(() => {
        this.$q.notify({
          message: 'Copied to clipboard!',
          color: 'green',
        });
      });
    },
  },
};
</script>
