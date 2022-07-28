<script>
    export default {
        data() {
            const classNames = [];
            if (this.className) {
                const className = this.className.split(" ");
                classNames.push(className);
            }

            if (this.isPrimary) {
                classNames.push("button-primary");
            }

            if (this.isWideMobile) {
                classNames.push("button-wide-mobile");
            }

            if (this.isSmall) {
                classNames.push("button-sm");
            }

            if (this.isBlock) {
                classNames.push("button-block");
            }

            return {
                classNames: classNames.join(" "),
            };
        },
        props: {
            className: String,
            isPrimary: Boolean,
            isWideMobile: Boolean,
            isSmall: Boolean,
            isBlock: Boolean,
        },
    };
</script>

<template>
    <button :class="classNames"><slot>Button</slot></button>
</template>

<style scoped></style>
