<script>
export default {
    name: "AppHeader",
    data() {
        return {
            activeNavElement: 0,
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
    },
    methods: {
        changeActive(index) {
            console.log("premut");
            this.navLinks[this.activeNavElement].active = true;
        }
    }
}
</script>

<template>
    <header class="header-section">
        <div class="container">
            <div class="header-container flex-between flex-v-center">
                <div class="logo-img">
                    <img src="../assets/img/dc-logo.png" alt="DC logo">
                </div>

                <nav>
                    <ul class="flex-v-center">
                        <li v-for="(link, index) in navLinks" :class="{ 'active': link.active }"
                            @click="changeActive(index)">
                            <!-- <a href="link.href">{{ link.label }}</a> -->
                            <a>{{ link.label }}</a>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
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
}

a {
    font-size: 0.8rem;
}

.active {
    border-bottom: 5px solid var(--col-light-blue);
}
</style>