<template>
    <div>
        <p>Quote</p>
        <input type="text" :value="newQuote" @input="updateNewQuote">
        <button @click="addQuote">Add Quote</button>
    </div>
</template>

<script>
    export default {
        data: () => {
            return {
                newQuote: ""
            }
        },
        methods: {
            updateNewQuote: function() {
                this.newQuote = event.target.value;         
            },
            addQuote: function() {
                if (this.newQuote !== '') { 
                    this.$emit('addQuote', this.newQuote)
                    this.newQuote = "";
                };
            }
        }
    }
</script>

<style scoped>

</style>