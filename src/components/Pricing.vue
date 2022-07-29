<script setup>
    import PricingItem from "../elements/PricingItem.vue";
    const pricings = [
        {
            id: 1,
            price: 27,
            desc: "Lorem ipsum is a common text",
            perks: [
                {
                    id: 1,
                    name: "Excepteur sint occaecat velit",
                    isChecked: true,
                },
                {
                    id: 2,
                    name: "Excepteur sint occaecat velit",
                    isChecked: true,
                },
                {
                    id: 3,
                    name: "Excepteur sint occaecat velit",
                    isChecked: true,
                },
                {
                    id: 4,
                    name: "Excepteur sint occaecat velit",
                    isChecked: false,
                },
                {
                    id: 5,
                    name: "Excepteur sint occaecat velit",
                    isChecked: false,
                },
            ],
        },
        {
            id: 2,
            price: 47,
            desc: "Lorem ipsum is a common text",
            perks: [
                {
                    id: 1,
                    name: "Excepteur sint occaecat velit",
                    isChecked: true,
                },
                {
                    id: 2,
                    name: "Excepteur sint occaecat velit",
                    isChecked: true,
                },
                {
                    id: 3,
                    name: "Excepteur sint occaecat velit",
                    isChecked: true,
                },
                {
                    id: 4,
                    name: "Excepteur sint occaecat velit",
                    isChecked: true,
                },
                {
                    id: 5,
                    name: "Excepteur sint occaecat velit",
                    isChecked: false,
                },
            ],
        },
        {
            id: 1,
            price: 67,
            desc: "Lorem ipsum is a common text",
            perks: [
                {
                    id: 1,
                    name: "Excepteur sint occaecat velit",
                    isChecked: true,
                },
                {
                    id: 2,
                    name: "Excepteur sint occaecat velit",
                    isChecked: true,
                },
                {
                    id: 3,
                    name: "Excepteur sint occaecat velit",
                    isChecked: true,
                },
                {
                    id: 4,
                    name: "Excepteur sint occaecat velit",
                    isChecked: true,
                },
                {
                    id: 5,
                    name: "Excepteur sint occaecat velit",
                    isChecked: true,
                },
            ],
        },
    ];
</script>

<template>
    <div class="container">
        <div class="pricing-inner section-inner has-top-divider">
            <div class="section-header center-content">
                <div class="container-xs">
                    <h2 class="mt-0 mb-16"> Simple, transarent pricing </h2>
                    <p class="m-0">
                        Lorem ipsum is common placeholder text used to
                        demonstrate the graphic elements of a document or visual
                        presentation.
                    </p>
                </div>
            </div>
            <div class="tiles-wrap">
                <PricingItem
                    v-for="item in pricings || []"
                    :item="item"
                    :key="item.id"
                ></PricingItem>
            </div>
        </div>
    </div>
</template>

<style scoped></style>
