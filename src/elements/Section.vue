<script setup>
    defineProps({
        className: String,
    });
</script>

<template>
    <section :class="className"><slot></slot></section>
</template>

<style scoped></style>
