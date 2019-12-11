<template>
    <div class="container">
        <QuotesBar :quotes="quotes"></QuotesBar>
        <QuotesInput @addQuote="addQuote"></QuotesInput>
        <QuotesView :quotes="quotes" @deleteQuote="deleteQuote"></QuotesView>
    </div>
</template>

<script>
    import QuotesBar from './components/QuotesBar.vue';
    import QuotesInput from './components/QuotesInput.vue';
    import QuotesView from './components/QuotesView.vue';

    export default {
        data: () => {
            return {
                quotes: []
            }
        },
        methods: {
            addQuote: function(newQuote) {
                if (this.quotes.length >= 10) {
                    alert("you reached the maximum of quotes")
                } else {
                    this.quotes.push(newQuote)                
                }
            },
            deleteQuote: function(index) {
                this.quotes.splice(index, 1)
            }
        },
        components: {
            QuotesBar,
            QuotesInput,
            QuotesView
        }
        
    }
</script>

<style>
</style>
