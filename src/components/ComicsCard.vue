<script>
export default {
    name: "ComicsCard",
    props: {
        comicSeries: String,
        comicImg: String
    }
}
</script>

<template>
    <section class="card">
        <div class="card-image">
            <img :src="comicImg" :alt="comicSeries">
        </div>
        <span class="card-text">
            {{ comicSeries }}
        </span>
    </section>
</template>


<style lang="scss" scoped>
.card {
    width: calc(100% / 6 - 1rem);
    margin: 0.5rem;
    display: flex;
    flex-direction: column;
}

.card-image {
    width: calc(80vw / 6 - 1rem);
    height: calc(80vw / 6 - 1rem);
    padding-bottom: 0.5rem;
    border: 1 solid black;

    img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: top;
    }
}

.card-text {
    display: block;
}
</style>