<template>
    <ul class="list-reset inline flex justify-center border-b-4 mb-0">
        <li class="p-4 inline bg-grey-lighter hover:bg-grey-light uppercase font-black cursor-pointer" v-for="category in categories" :key="category"> {{ category }}</li>
        <li lass="p-4 inline bg-grey-lighter hover:bg-grey-light uppercase font-black cursor-pointer" @click="triggerShowAddCategory">+</li>
    </ul>
</template>
<script>
    export default {
        props: ['categories'],
        methods: {
            triggerShowAddCategory() {
                this.$emit('triggerShowAddCategory')
            }
        }
    }
</script>