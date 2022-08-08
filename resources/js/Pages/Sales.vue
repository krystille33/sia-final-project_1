<template>
    <h1 class="text-center">Sales</h1>
    <hr />
    <div class="container">
        <div class="d-flex align-content-between">
            <table class="table table-dark">
                <thead>
                    <tr>
                        <th scope="col">#</th>
                        <th scope="col">Daily</th>
                        <th scope="col">Weekly</th>
                        <th scope="col">Monthly</th>
                        <th scope="col">Yearly</th>
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="sale in sales" :key="sale.id">
                        <td>{{ sale.id }}</td>
                        <td>{{ sale.daily_sales }}</td>
                        <td>{{ sale.weekly_sales }}</td>
                        <td>{{ sale.monthly_sales }}</td>
                        <td>{{ sale.yearly_sales }}</td>
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
        sales: Array,
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
