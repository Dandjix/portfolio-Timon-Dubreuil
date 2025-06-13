import { default } from '../content/StageS5.vue';
<template>
    <div class="full-width" style="display: flex; justify-content: center; align-items: center;">
        <q-card class="q-pa-md q-my-lg sectionCard" :style="`max-width:${maxWidth};`">
            <slot></slot>
        </q-card>
    </div>
</template>

<style scoped>
.sectionCard {
    border-radius: 20px;
}
</style>

<script>
export default {
    props: {
        maxWidth: {
            type: String,
            default: "1300px"
        }
    }
}
</script>