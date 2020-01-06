<template>
    <table class="table">
        <thead class="bg-blue text-white">
            <tr>
                <th scope="col">Date</th>
                <th scope="col">Amount</th>
                <th scope="col">Category</th>
                <th scope="col"></th>
            </tr>
        </thead>
        <tbody>
            <tr v-for="(bill, index) in bills" :key="index" class="p-4">
                <td>{{bill.date}}</td>
                <td>{{bill.amount}}</td>
                <td>{{bill.category}}</td>
            </tr>
        </tbody>
    </table>
</template>
<script>
export default {
    name: 'BillsTable',
    props: ['bills']
}
</script>