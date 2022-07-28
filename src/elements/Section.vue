<script setup>
    defineProps({
        class: {
            type: String,
        },
    });
</script>

<template>
    <section :class="class"><slot>Section</slot></section>
</template>

<style scoped></style>
