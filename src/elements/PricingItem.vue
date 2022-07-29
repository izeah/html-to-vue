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
        computed: {
            sanitizeItemID() {
                return typeof this.item.id !== "undefined"
                    ? this.item.id
                    : Math.random() * 999999999;
            },
            sanitizeItemPrice() {
                return typeof this.item.price !== "undefined"
                    ? this.item.price
                    : 0;
            },
            sanitizeItemDesc() {
                return typeof this.item.desc !== "undefined"
                    ? this.item.desc
                    : "[NO DESCRIPTION]";
            },
            sanitizeItemPerks() {
                return typeof this.item.perks !== "undefined"
                    ? this.item.perks
                    : [];
            },
        },
    };
</script>

<template>
    <div class="tiles-item">
        <div class="tiles-item-inner has-shadow" :key="sanitizeItemID">
            <div class="pricing-item-content">
                <div class="pricing-item-header pb-24 mb-24">
                    <div class="pricing-item-price mb-4">
                        <span class="pricing-item-price-currency h2">$</span
                        ><span
                            class="pricing-item-price-amount h1 pricing-switchable"
                            >{{ sanitizeItemPrice }}</span
                        >
                    </div>
                    <div class="text-xs text-color-low">
                        {{ sanitizeItemDesc }}
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
                            v-for="perk in sanitizeItemPerks"
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
