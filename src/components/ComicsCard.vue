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
    <div class="card-image">
        <img :src="comicImg" :alt.uppercase="comicSeries">
    </div>
    <span class="card-text">
        {{ comicSeries }}
    </span>
</template>

<style lang="sass" scoped>

</style>