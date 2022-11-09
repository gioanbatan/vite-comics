<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import AppBanner from "./components/AppBanner.vue";
import AppFooter from "./components/AppFooter.vue";
import ComicsCard from "./components/ComicsCard.vue";

export default {
  components: {
    AppHeader,
    AppMain,
    AppBanner,
    AppFooter,
    ComicsCard
  }
}
</script>

<template>
  <AppHeader />
  <AppMain />
  <AppBanner />
  <AppFooter />
</template>

<style lang="scss">
@use "./style/general.scss" as *;
@use "./style/partials/variables" as *;
</style>