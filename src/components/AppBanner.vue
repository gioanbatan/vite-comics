<script>
export default {
    name: "AppBanner",
    data() {
        return {
            bannerElements: [
                {
                    name: "DIGITAL COMICS",
                    image: "buy-comics-digital-comics.png",
                    href: "#"
                },
                {
                    name: "DC MERCHANDISE",
                    image: "buy-comics-merchandise.png",
                    href: "#"
                },
                {
                    name: "SUBSCRIPTIONS",
                    image: "buy-comics-subscriptions.png",
                    href: "#"
                },
                {
                    name: "COMIC SHOP LOCATOR",
                    image: "buy-comics-shop-locator.png",
                    href: "#"
                },
                {
                    name: "DC POWER VISA",
                    image: "buy-dc-power-visa.svg",
                    href: "#"
                },
            ]
        }
    },
    methods: {
        getImagePath(imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    }
}
</script>

<template>
    <div class="banner-section">
        <div class="container">
            <div class="banner-container flex-v-center">
                <ul class="flex-between flex-v-center">
                    <li v-for="link in bannerElements">
                        <a class="flex-v-center" :href="link.href">
                            <img :src="getImagePath(`../assets/img/${link.image}`)" :alt="link.name">
                            <span>{{ link.name }}</span>
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.banner-section {
    width: 100%;
    background-color: var(--col-light-blue);
}

.banner-container {
    width: 100%;
    height: 200px;

    font-size: 0.9rem;
    color: var(--col-white);
}

ul {
    width: 100%;
    padding: 0 1rem;
}

a img {
    max-width: 50px;
    max-height: 50px;
}

a span {
    display: block;
    padding-left: 1rem;
}
</style>