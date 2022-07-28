<script>
    export default {
        data() {
            return {
                items: [
                    {
                        id: 1,
                        img_url: "src/assets/images/clients-01.svg",
                        img_alt: "Clients 01",
                    },
                    {
                        id: 2,
                        img_url: "src/assets/images/clients-02.svg",
                        img_alt: "Clients 02",
                    },
                    {
                        id: 3,
                        img_url: "src/assets/images/clients-03.svg",
                        img_alt: "Clients 03",
                    },
                    {
                        id: 4,
                        img_url: "src/assets/images/clients-04.svg",
                        img_alt: "Clients 04",
                    },
                    {
                        id: 5,
                        img_url: "src/assets/images/clients-05.svg",
                        img_alt: "Clients 05",
                    },
                ],
            };
        },
    };
</script>

<template>
    <div class="container">
        <div
            class="clients-inner section-inner has-top-divider has-bottom-divider"
        >
            <ul class="list-reset">
                <li v-for="item in items" :key="item.id">
                    <img :src="item.img_url" :alt="item.img_alt" />
                </li>
            </ul>
        </div>
    </div>
</template>

<style scoped></style>
