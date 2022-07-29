<script setup>
    const props = defineProps({
        className: String,
        isPrimary: Boolean,
        isWideMobile: Boolean,
        isSmall: Boolean,
        isBlock: Boolean,
    });

    const classNames = [];
    if (props.className) {
        const className = props.className.split(" ");
        classNames.push(className);
    }

    if (props.isPrimary) {
        classNames.push("button-primary");
    }

    if (props.isWideMobile) {
        classNames.push("button-wide-mobile");
    }

    if (props.isSmall) {
        classNames.push("button-sm");
    }

    if (props.isBlock) {
        classNames.push("button-block");
    }
</script>

<template>
    <button :class="classNames"><slot>Button</slot></button>
</template>

<style scoped></style>
