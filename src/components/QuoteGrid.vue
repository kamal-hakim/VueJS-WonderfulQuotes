<template>
    <div class="row">
        <app-quote v-for="(quote, index) in quotes" :key="quote.id" @click.native="deleteQuote(index)">{{ quote }}</app-quote>
    </div>
</template>

<script>
    import Quote from './Quotes.vue';

    export default {
        props: ['quotes'],
        methods: {
            deleteQuote(index) {
                this.$emit('quoteDeleted', index);
            }
        },
        components: {
            appQuote: Quote
        },
    }
</script>

<style>

</style>
