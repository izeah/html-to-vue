<script setup>
    defineProps({
        className: String,
    });
</script>

<template>
    <section :class="className"><slot>Section</slot></section>
</template>

<style scoped></style>
