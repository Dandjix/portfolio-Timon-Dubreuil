<template>
  <!-- <div class="q-px-lg q-py-md">
    <q-timeline layout="dense" color="secondary">
      <q-timeline-entry v-for="(entry, i) in entries" :key="i" :title=entry.title :subtitle="entry.subtitle">
        <div style="display: flex; align-items: center; gap: 1rem;">
          <SAE v-if="entry.content == 'SAE'" />
          <StageS5 v-if="entry.content == 'StageS5'" />
        </div>
      </q-timeline-entry>
    </q-timeline>
  </div> -->
  <div>
    <StageS5 />
  </div>

</template>

<script>
// import SAE from 'src/components/content/SAE.vue';
import StageS5 from 'src/components/content/StageS5.vue';

export default {
  components: {
    // SAE,
    StageS5
  },
  // data() {
  //   return {
  //     entries: [
  //       {
  //         title: "SAE",
  //         subtitle: "Octobre 2024 - Juin 2025",
  //         content: "SAE"
  //       },
  //       {
  //         title: "Stage",
  //         subtitle: "Janvier 2025 - Mai 2025",
  //         content: "StageS5"
  //       },
  //     ]
  //   }
  // }

}
</script>