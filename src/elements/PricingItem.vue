<script>
    import Button from "./Button.vue";
    export default {
        props: {
            item: {
                type: Object,
                required: true,
            },
        },
        components: {
            Button,
        },
    };
</script>

<template>
    <div class="tiles-item">
        <div class="tiles-item-inner has-shadow" :key="item?.id || 0">
            <div class="pricing-item-content">
                <div class="pricing-item-header pb-24 mb-24">
                    <div class="pricing-item-price mb-4">
                        <span class="pricing-item-price-currency h2">$</span
                        ><span
                            class="pricing-item-price-amount h1 pricing-switchable"
                            >{{ item?.price || 0 }}</span
                        >
                    </div>
                    <div class="text-xs text-color-low">
                        {{ item?.desc || "Lorem Ipsum Dolor Sit Amet" }}
                    </div>
                </div>
                <div class="pricing-item-features mb-40">
                    <div
                        class="pricing-item-features-title h6 text-xs text-color-high mb-24"
                    >
                        What’s included
                    </div>
                    <ul
                        class="pricing-item-features-list list-reset text-xs mb-32"
                    >
                        <li
                            v-for="perk in item?.perks || []"
                            :class="perk.isChecked ? 'is-checked' : ''"
                            :key="perk.id"
                        >
                            {{ perk.name }}
                        </li>
                    </ul>
                </div>
            </div>
            <div class="pricing-item-cta mb-8">
                <Button className="button" isPrimary isBlock
                    >Start free trial</Button
                >
            </div>
        </div>
    </div>
</template>

<style scoped></style>
