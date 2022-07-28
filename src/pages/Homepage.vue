<script setup>
    import Clients from "../components/Clients.vue";
    import Features from "../components/Features.vue";
    import Footer from "../components/Footer.vue";
    import Header from "../components/Header.vue";
    import Hero from "../components/Hero.vue";
    import Pricing from "../components/Pricing.vue";
    import Section from "../elements/Section.vue";
</script>

<template>
    <div class="body-wrap">
        <Header></Header>
        <main class="site-content">
            <Section
                class="section hero center-content illustration-section-01"
            >
                <Hero></Hero>
            </Section>
            <Section class="section clients">
                <Clients></Clients>
            </Section>
            <Section class="section features-tiles">
                <Features></Features>
            </Section>
            <Section class="section pricing">
                <Pricing></Pricing>
            </Section>
        </main>
        <Footer></Footer>
    </div>
</template>

<style scoped></style>
