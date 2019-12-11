<template>
    <div>
        Inside View
        <div 
            v-for="(quote, index) in quotes"
            :key="index"
            @click="deleteQuote(index)"
            >
                {{quote}}
        </div>
    </div>
</template>

<script>
    export default {
        props: {
            quotes: Array
        },
        methods: {
            deleteQuote: function(index) {
                this.$emit('deleteQuote', index)
            }
        }

    }
</script>

<style scoped>

</style>