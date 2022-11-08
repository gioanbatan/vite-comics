<script>
export default {
    name: "AppHeader",
    data() {
        return {
            navLinks: [
                {
                    label: "CHARACTERS",
                    href: "",
                    active: true,
                },
                {
                    label: "COMICS",
                    href: "",
                    active: false,
                },
                {
                    label: "MOVIES",
                    href: "",
                    active: false,
                },
                {
                    label: "TV",
                    href: "",
                    active: false,
                },
                {
                    label: "GAMES",
                    href: "",
                    active: false,
                },
                {
                    label: "COLLECTIBLES",
                    href: "",
                    active: false,
                },
                {
                    label: "VIDEOS",
                    href: "",
                    active: false,
                },
                {
                    label: "FANS",
                    href: "",
                    active: false,
                },
                {
                    label: "NEWS",
                    href: "",
                    active: false,
                },
                {
                    label: "SHOP",
                    href: "",
                    active: false,
                }
            ]
        }
    }
}
</script>

<template>
    <section class="header-section">
        <div class="container">
            <div class="header-container flex-between flex-v-center">
                <div class="logo-img">
                    <img src="../assets/img/dc-logo.png" alt="DC logo">
                </div>

                <nav>
                    <ul class="flex-v-center">
                        <li v-for="link in navLinks" :class="link.active ? 'active' : ''">
                            <a href="link.href">{{ link.label }}</a>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>
    </section>
</template>

<style scoped>
.header-section {
    width: 100%;
    margin: 0 auto;
    background-color: var(--col-white);
}

.header-container {
    height: 120px;
}

.logo-img {
    width: 110px;
    padding: 1rem;
}

nav {
    height: 100%;
}

ul {
    height: 100%;
}

li {
    display: flex;
    align-items: center;
    height: 100%;
    padding: 1rem;

    /* DEBUG */
    border: 2px dashed brown;
}

a {
    font-size: 0.8rem;
}

.active {
    border-bottom: 5px solid var(--col-light-blue);
}
</style>