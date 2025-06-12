<template>
  <q-item clickable style="width: fit-content;" @click="copyToClipboard()">
    <div style="display: flex; align-items: center; justify-content: center;">
      <q-icon :name="icon" class="q-pr-sm" />

      <span>{{ value }}</span>
    </div>
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
          message: `${this.name} copié(e) dans le presse-papier!`,
          color: 'green',
        });
      });
    },
  },
};
</script>
