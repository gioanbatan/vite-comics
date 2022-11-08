<script>
export default {
    name: "AppBanner",
    data() {
        return {
            bannerElements: [
                {
                    name: "DIGITAL COMICS",
                    image: "url.image",
                }
            ]
        }
    }
}
</script>

<template>
    <div class="banner-section">
        <div class="container">
            <div class="banner-container flex-v-center">
                <ul class="flex-between">
                    <li>
                        <a class="flex-v-center" href="">
                            <img src="../assets/img/buy-comics-digital-comics.png" alt="">
                            <span>TEST</span>
                        </a>
                    </li>

                    <li>
                        <a class="flex-v-center" href="">
                            <img src="../assets/img/buy-comics-digital-comics.png" alt="">
                            <span>TEST</span>
                        </a>
                    </li>
                    <li>
                        <a class="flex-v-center" href="">
                            <img src="../assets/img/buy-comics-digital-comics.png" alt="">
                            <span>TEST</span>
                        </a>
                    </li>
                    <li>
                        <a class="flex-v-center" href="">
                            <img src="../assets/img/buy-comics-digital-comics.png" alt="">
                            <span>TEST</span>
                        </a>
                    </li>
                    <li>
                        <a class="flex-v-center" href="">
                            <img src="../assets/img/buy-comics-digital-comics.png" alt="">
                            <span>TEST</span>
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>

<style scoped>
.banner-section {
    width: 100%;
    background-color: var(--col-light-blue);
}

.banner-container {
    width: 100%;
    height: 200px;

    color: var(--col-white);
}

ul {
    width: 100%;
}

a img {
    width: 40px;
}

a span {
    padding-left: 1rem;
}
</style>