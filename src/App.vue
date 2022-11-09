<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import AppBanner from "./components/AppBanner.vue";
import AppFooter from "./components/AppFooter.vue";

export default {
  components: {
    AppHeader,
    AppMain,
    AppBanner,
    AppFooter
  }
}
</script>

<template>
  <AppHeader />
  <AppMain />
  <AppBanner />
  <AppFooter />
</template>

<style>
/* RESET */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

img {
  max-width: 100%;
}

a {
  text-decoration: none;
  color: inherit;
}

li {
  list-style: none;
}

/* VARIABLES */
:root {
  /* Colors */
  --col-white: #ffffff;
  --col-light-blue: #3b7df6;
  --col-dark-gray: #212121;
  --col-gray: #323232;
  --col-light-gray: #939393;
}

/* UTILITIES */
.flex-v-center {
  display: flex;
  align-items: center;
}

.flex-between {
  display: flex;
  justify-content: space-between;
}

/* COMMON */
.container {
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
}
</style>