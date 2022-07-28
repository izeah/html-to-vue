<script setup>
    defineProps({
        item: {
            type: Object,
            required: true,
        },
    });
</script>

<template>
    <div class="tiles-item">
        <div class="tiles-item-inner">
            <div class="features-tiles-item-header">
                <div class="features-tiles-item-image mb-16">
                    <img
                        :src="
                            item?.img_url ||
                            '../assets/images/feature-tile-icon-01.svg'
                        "
                        :alt="item?.img_alt"
                        width="64"
                        height="64"
                    />
                </div>
            </div>
            <div class="features-tiles-item-content">
                <h4 class="mt-0 mb-8">
                    {{ item?.title || "Lorem Ipsum" }}
                </h4>
                <p class="m-0 text-sm">
                    {{ item?.desc || "Lorem Ipsum Dolor Sit Amet" }}
                </p>
            </div>
        </div>
    </div>
</template>

<style scoped></style>
