<template>
    <h1 class="text-center">Owner Page</h1>
    <hr />
    <div class="container">
        <div class="d-flex align-content-between">
            <table class="table table-striped">
                <thead>
                    <tr>
                        <th scope="col">#</th>
                        <th scope="col">Name</th>
                        <th scope="col">Address</th>
                        <th scope="col">Contact</th>
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="owner in owners" :key="owner.id">
                        <td>{{ owner.id }}</td>
                        <td>{{ owner.firstname }}</td>
                        <td>{{ owner.lastname }}</td>
                        <td>{{ owner.contact }}</td>
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
        owners: Array,
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
