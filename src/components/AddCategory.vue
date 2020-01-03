<template>
    <div class="h-100 w-full flex items-center justify-center font-sans"> 
        <div class="bg-white rounded shadow p-6 m-4 w-full lg:w-3/4 lg:max-w-lg">
            <div class="mb-4">
                <h1>Opprett ny kategori</h1>
                <p>Eks. 'Strøm', 'Bensin' eller 'Internett'</p>
                <div class="flex mt-4">
                    <input class="shadow appearance-none border rounded w-full py-2 px-3 mr-4 text-grey-darker" placeholder="Opprett kategori" v-model="category">
                    <button class="flex-no-shrink p-2 border-2 rounded bg-teal text-white border-teal hover:text-white hover:bg-teal" @click="handleClick">Lag</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'AddCategory',
        data: function() {
            return {
                category: ''
            }
        },
        methods: {
            handleClick: function() {
                if(!this.category) {
                    alert('Skriv inn en kategori')
                    return
                }

                this.$emit('addCategory', this.category)
            }
        }
    }
</script>