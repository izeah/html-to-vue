<script setup>
    import Button from "../elements/Button.vue";
</script>

<template>
    <header class="site-header">
        <div class="container">
            <div class="site-header-inner">
                <div class="brand">
                    <h1 class="m-0">
                        <a href="#"
                            ><img
                                src="../assets/images/logo.svg"
                                alt="Cube"
                                width="32"
                                height="32"
                        /></a>
                    </h1>
                </div>
                <Button className="header-nav-toggle"
                    ><span class="screen-reader">Menu</span>
                    <span class="hamburger"
                        ><span class="hamburger-inner"></span></span
                ></Button>
                <nav id="header-nav" class="header-nav">
                    <div class="header-nav-inner">
                        <ul class="list-reset text-xxs header-nav-right">
                            <li><a href="#">Home</a></li>
                            <li><a href="#">Features</a></li>
                            <li><a href="#">Pricing</a></li>
                            <li><a href="#">Showcase</a></li>
                        </ul>
                        <ul class="list-reset header-nav-right">
                            <li>
                                <Button
                                    className="button"
                                    isPrimary
                                    isWideMobile
                                    isSmall
                                    >Sign up</Button
                                >
                            </li>
                        </ul>
                    </div>
                </nav>
            </div>
        </div>
    </header>
</template>

<style scoped></style>
