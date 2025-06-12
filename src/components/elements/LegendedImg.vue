<template>
    <div class="legended-img" :class="imgClass" v-bind="$attrs">
        <img :src="src" :alt="alt" class="img-fluid" :width="width" />
        <p class="legend">{{ alt }}</p>
    </div>
</template>

<script>
export default {
    inheritAttrs: false,
    props: {
        src: { type: String, required: true },
        alt: { type: String, required: true },
        imgClass: { type: [String, Array, Object], default: '' },
        width: { type: [Number, String], default: null }
    }
}
</script>

<style scoped>
.legended-img {
    position: relative;
    /* anchor for absolute legend */
    display: block;
    /* respect layout flow */
    width: 100%;
    /* take full width of container */
}

.legended-img img {
    display: block;
    /* remove img bottom gap */
    width: 100%;
    /* responsive image */
    height: auto;
}

.legend {
    position: absolute;
    bottom: 10px;
    left: 26px;
    right: 26px;
    color: white;
    background: rgba(0, 0, 0, 0.9);
    padding: 4px 8px;
    font-size: 0.9em;
    border-radius: 4px;
    pointer-events: none;
    user-select: none;
}
</style>
