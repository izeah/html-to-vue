<script setup>
    import FeatureItem from "../elements/FeatureItem.vue";
    const features = [
        {
            id: 1,
            img_url: "src/assets/images/feature-tile-icon-01.svg",
            img_alt: "Feature tile icon 01",
            title: "Join the system",
            desc: `A pseudo-Latin text used in web design, layout, and
                    printing in place of things to emphasise design.`,
        },
        {
            id: 2,
            img_url: "src/assets/images/feature-tile-icon-01.svg",
            img_alt: "Feature tile icon 02",
            title: "Join the system",
            desc: `A pseudo-Latin text used in web design, layout, and
                    printing in place of things to emphasise design.`,
        },
        {
            id: 3,
            img_url: "src/assets/images/feature-tile-icon-03.svg",
            img_alt: "Feature tile icon 03",
            title: "Join the system",
            desc: `A pseudo-Latin text used in web design, layout, and
                    printing in place of things to emphasise design.`,
        },
    ];
</script>

<template>
    <div class="container">
        <div class="features-tiles-inner section-inner">
            <div class="tiles-wrap">
                <FeatureItem
                    v-for="item in features"
                    :key="item.id"
                    :item="item"
                ></FeatureItem>
            </div>
        </div>
    </div>
</template>

<style scoped></style>
