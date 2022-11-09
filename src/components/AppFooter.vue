<script>
export default {
    name: "AppFooter",
    data() {
        return {
            footerLinks: {
                linksDCComics: [
                    {
                        link: "Character",
                        href: ""
                    },
                    {
                        link: "Comics",
                        href: ""
                    },
                    {
                        link: "Movies",
                        href: ""
                    },
                    {
                        link: "TV",
                        href: ""
                    },
                    {
                        link: "Games",
                        href: ""
                    },
                    {
                        link: "Videos",
                        href: ""
                    },
                    {
                        link: "News",
                        href: ""
                    }
                ],
                linksShop: [
                    {
                        link: "Shop SC",
                        href: ""
                    },
                    {
                        link: "Shop DC Collectibles",
                        href: ""
                    }
                ],
                linksDC: [
                    {
                        link: "Term Of Use",
                        href: ""
                    },
                    {
                        link: "Privaci policy (New)",
                        href: ""
                    },
                    {
                        link: "Ad Choices",
                        href: ""
                    },
                    {
                        link: "Advertising",
                        href: ""
                    },
                    {
                        link: "Jobs",
                        href: ""
                    },
                    {
                        link: "Subscriptions",
                        href: ""
                    },
                    {
                        link: "Talent Workshops",
                        href: ""
                    },
                    {
                        link: "CPSC Certificates",
                        href: ""
                    },
                    {
                        link: "Ratings",
                        href: ""
                    },
                    {
                        link: "Shop Help",
                        href: ""
                    },
                    {
                        link: "Contact Us",
                        href: ""
                    }
                ],
                linksSites: [
                    {
                        link: "DC",
                        href: ""
                    },
                    {
                        link: "MAD Magazine",
                        href: ""
                    },
                    {
                        link: "DC Kids",
                        href: ""
                    },
                    {
                        link: "DC Universe",
                        href: ""
                    },
                    {
                        link: "DC Power Visa",
                        href: ""
                    }
                ]
            }
        }
    }
}
</script>

<template>
    <footer class="footer-section">
        <div class="container">
            <div class="footer-container flex-between">
                <div class="links-lists">
                    <ul>
                        <li>DC COMICS</li>
                        <li v-for="links in footerLinks.linksDCComics">
                            <a :href="links.href">{{ links.link }}</a>
                        </li>
                    </ul>

                    <ul>
                        <li>SHOP</li>
                        <li v-for="links in footerLinks.linksShop">
                            <a :href="links.href">{{ links.link }}</a>
                        </li>
                    </ul>

                    <ul>
                        <li>DC</li>
                        <li v-for="links in footerLinks.linksDC">
                            <a :href="links.href">{{ links.link }}</a>
                        </li>
                    </ul>

                    <ul>
                        <li>SITES</li>
                        <li v-for="links in footerLinks.linksSites">
                            <a :href="links.href">{{ links.link }}</a>
                        </li>
                    </ul>
                </div>

                <div class="logo-dc-bg">
                    <img src="../assets/img/dc-logo-bg.png" alt="Logo DC">
                </div>
            </div>
        </div>

        <section class="footer-bottom">
            <div class="container">
                <div class="footer-bottom-container flex-between flex-v-center">
                    <button class="btn">SIGN-UP NOW!</button>

                    <div class="social flex-v-center">
                        <span class="follow-us">FOLLOW US</span>
                        <a href="">
                            <img src="../assets/img/footer-facebook.png" alt="Facebook">
                        </a>

                        <a href="">
                            <img src="../assets/img/footer-twitter.png" alt="Twitter">
                        </a>

                        <a href="">
                            <img src="../assets/img/footer-youtube.png" alt="YouTube">
                        </a>

                        <a href="">
                            <img src="../assets/img/footer-pinterest.png" alt="Pinterest">
                        </a>

                        <a href="">
                            <img src="../assets/img/footer-periscope.png" alt="Periscope">
                        </a>
                    </div>
                </div>
            </div>
        </section>
    </footer>

</template>

<style lang="scss" scoped>
.footer-section {
    background-color: var(--col-dark-gray);
    background-image: url(../assets/img/footer-bg.jpg);
    background-position: center;
    background-size: cover;
}

.footer-container {
    /* width: 100%; */

    /* DEBUG */
    height: 550px;
}

.links-lists {
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    align-items: flex-start;
    padding: 2rem 0;
    color: var(--col-white);
}

ul {
    padding: 1rem 2rem 1rem 0;
}

li:first-child {
    font-weight: 900;
}

li:not(:first-child) {
    color: var(--col-light-gray);
}

li {
    padding: 0.4rem 0;
}

li:last-child {
    padding-bottom: 1rem;
}

.logo-dc-bg {
    position: relative;
    width: 50%;
    height: 100%;
    overflow: hidden;
}

.logo-dc-bg img {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}

.footer-bottom {
    width: 100%;

    background-color: var(--col-gray);
}

.footer-bottom-container {
    width: 100%;
    height: 100px;
}

.btn {
    font-size: 1.2rem;
    font-weight: 500;
    padding: 1.3rem;
    border: 3px solid #3b7df6;
    color: var(--col-white);
    background-color: inherit;
    cursor: pointer;
}

.follow-us {
    color: var(--col-light-blue);
}

.social>* {
    padding-left: 1rem;
}
</style>