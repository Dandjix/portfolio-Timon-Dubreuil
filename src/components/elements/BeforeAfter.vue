import { default } from '../../layouts/MainLayout.vue';
<template>
    <div class="row items-center q-py-md">
        <img :src="before" alt="Page du schéma interactif (Avant)" class="col-12 col-md-5" />

        <div class="col-2 gt-sm flex justify-center">
            <q-icon name="arrow_forward" size="lg" />
        </div>

        <div class="col-12 lt-md flex justify-center">
            <q-icon name="arrow_downward" size="lg" />
        </div>

        <img :src="after" alt="Page du schéma interactif (Après)" class="col-12 col-md-5" />
    </div>
</template>

<style scoped>
img {
    border-radius: 12px;
}
</style>

<script>
export default {
    props: {
        before: { type: String, required: true },
        after: { type: String, required: true }
    }
}
</script>