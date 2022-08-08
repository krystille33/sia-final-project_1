<template>
    <h1 class="text-center">House Page</h1>
    <hr />
    <div class="container">
        <div class="d-flex align-content-between">
            <table class="table table-striped">
                <thead>
                    <tr>
                        <th scope="col">#</th>
                        <th scope="col">Name</th>
                        <th scope="col">Address</th>
                        <th scope="col">Price</th>
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="house in houses" :key="house.id">
                        <td>{{ house.id }}</td>
                        <td>{{ house.name }}</td>
                        <td>{{ house.address }}</td>
                        <td>{{ house.price }}</td>
                    </tr>
                </tbody>
            </table>
        </div>
    </div>
</template>

<script setup>
import NavBar from "../Shared/NavBar.vue";
</script>
<script>
export default {
    layout: NavBar,
    props: {
        houses: Array,
    },
};
</script>
<style scoped>
.card-style {
    width: 500px;
    height: 200px;
}
.price {
    position: absolute;
    bottom: 0px;
    right: 0px;
}
</style>
