<template>
  <!-- <div class="q-px-lg q-py-md">
    <q-timeline layout="dense" color="secondary">
      <q-timeline-entry v-for="(entry, i) in entries" :key="i" :title=entry.title :subtitle="entry.subtitle">
        <div style="display: flex; align-items: center; gap: 1rem;">
          <SAE v-if="entry.content == 'SAE'" />
          <StageS6 v-if="entry.content == 'StageS6'" />
        </div>
      </q-timeline-entry>
    </q-timeline>
  </div> -->
  <div>
    <StageS6 />
  </div>

</template>

<script>
// import SAE from 'src/components/content/SAE.vue';
import StageS6 from 'src/components/content/StageS6.vue';

export default {
  components: {
    // SAE,
    StageS6
  },
  data() {
    return {
      entries: [
        {
          title: "SAE",
          subtitle: "Octobre 2024 - Juin 2025",
          content: "SAE"
        },
        {
          title: "Stage",
          subtitle: "Janvier 2025 - Mai 2025",
          content: "StageS6"
        },
      ]
    }
  }

}
</script>