<script>
export default {
    name: "AppMain",
    data() {
        return {
            comicsDC: [
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel"
                }
            ]
        }
    }
}
</script>

<template>
    <section class="header-main">
        <div class="container">
            <h2>CURRENT SERIES</h2>
        </div>
    </section>

    <section class="main-container">
        <div class="container">
            <div class="row">
                <div class="col">
                    <div class="card" v-for="(comic, index) in comicsDC" :key="index">
                        <div class="card-image">
                            <img :src="comic.thumb" :alt.uppercase="comic.series">
                        </div>
                        <span class="card-text">
                            {{ comic.series }}
                        </span>
                    </div>
                </div>
            </div>

            <button class="btn-std">load more</button>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;

.header-main {
    position: relative;
    background-image: url(../assets/img/jumbotron.jpg);
    background-position: top;
    background-size: cover;
    height: 300px;

    h2 {
        font-family: 'Open Sans condensed', sans-serif;
        display: block;
        position: absolute;
        bottom: -1.2rem;
        text-transform: uppercase;
        color: $col_white;
        background-color: $col_light_blue;
        font-stretch: condensed;
        font-size: 1.3rem;
        padding: 0.7rem;
    }
}

.main-container {
    background-color: $col_dark_gray;
    color: $col_white;
    padding: 2rem;
}

.col {
    display: flex;
    flex-wrap: wrap;
}

.card {
    width: calc(100% / 6 - 1rem);
    margin: 0.5rem;

    .card-image {
        width: calc(80vw / 6 - 1rem);
        height: calc(80vw / 6 - 1rem);
        padding-bottom: 0.5rem;

        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: top;
        }
    }

    .card-text {
        font-size: 0.8rem;
        text-transform: uppercase;
    }
}

.btn-std {
    display: block;
    margin: 1rem auto;
}
</style>