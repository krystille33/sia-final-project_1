<template>
    <div class="sidebar bg-light m-2 shadow-lg bg-white center">
        <Link
            class="p-2 links mr-1"
            :class="{ active: $page.component == 'Home' }"
            href="/"
            >Home
        </Link>

        <Link
            class="p-2 mr-1"
            :class="{ active: $page.component == 'Owner' }"
            href="/owners"
            >Owner</Link
        >
        <Link
            class="p-2 mr-1"
            :class="{ active: $page.component == 'House' }"
            href="/houses"
            >House</Link
        >
    </div>

    <slot />
</template>
<script setup>
import { Link } from "@inertiajs/inertia-vue3";
</script>

<script>
export default {
    data() {
        return {
            layout: false,
        };
    },
};
</script>

<style scoped>
.links {
}
.sidebar a.active {
    background-color: #3f15d6;
    color: white;
    text-decoration: none;
}

.sidebar a:hover:not(.active) {
    background-color: rgb(189, 177, 253);
    color: white;
    text-decoration: none;
}
.center {
    display: flex;
    align-items: center;
    justify-content: end;
}
</style>
