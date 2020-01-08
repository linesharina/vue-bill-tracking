<template>
    <ul class="list-reset inline flex justify-center border-b-4 mb-0">
        <li class="p-4 inline hover:bg-gray-300 uppercase font-black cursor-pointer" :class="[activeCategory === '' ? 'bg-gray-500' : 'bg-gray-200']" @click="clearActiveCategory()">All</li>
        <li class="p-4 inline bg-gray-200 hover:bg-gray-300 uppercase font-black cursor-pointer" :class="[ activeCategory === category ? 'bg-gray-500' : 'bg-gray-200']" v-for="category in categories" :key="category" @click="setActiveCategory(category)"> {{ category }}</li>
        <li lass="p-4 inline bg-grey-lighter hover:bg-grey-light uppercase font-black cursor-pointer" @click="triggerShowAddCategory">+</li>
    </ul>
</template>
<script>
    export default {
        props: ['categories', 'activeCategory'],
        methods: {
            triggerShowAddCategory() {
                this.$emit('triggerShowAddCategory')
            },
            clearActiveCategory() {
                this.$emit('clearActiveCategory')
            },
            setActiveCategory(category) {
                this.$emit('setActiveCategory', category)
            }
        }
    }
</script>