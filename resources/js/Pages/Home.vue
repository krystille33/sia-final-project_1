<template>
    <div class="home"></div>
</template>
<script setup>
import NavBar from "../Shared/NavBar.vue";
</script>

<script>
export default {
    layout: NavBar,
};
</script>
<style scoped>
.h1 {
    font-size: 100px;
    margin: none;
}
.home {
    background-image: url("../Pages/images/bike-g1c38c27cf_1280.jpg");
    background-position: center;
    background-size: cover;
    height: 100vh;
    overflow: hidden;
}
</style>
