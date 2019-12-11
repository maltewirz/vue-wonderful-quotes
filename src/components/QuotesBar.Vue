<template>
    <div>
        Quotes added: {{quotes.length}} / 10
    </div>
</template>

<script>
    export default {
        props: {
            quotes: Array
        },
        
    }
</script>

<style scoped>

</style>