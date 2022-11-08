<script>
export default {
    name: "AppHeader",
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
                        <li class="active"><a href="">test</a></li>
                        <li><a href="">test</a></li>
                        <li><a href="">test</a></li>
                        <li><a href="">test</a></li>
                        <li><a href="">test</a></li>
                        <li><a href="">test</a></li>
                        <li><a href="">test</a></li>
                        <li><a href="">test</a></li>
                        <li><a href="">test</a></li>
                        <li><a href="">test</a></li>
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

.active {
    border-bottom: 5px solid var(--col-light-blue);
}
</style>