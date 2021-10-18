<template>
    <div class="container">
        <app-header :quoteCount="quotes.length" :maxQuotes="maxQuotes"></app-header>

        <appNewQuote @quoteadded="newQuote"></appNewQuote>
        <app-body-quote @quoteDeleted="deleteQuote" :quotes="quotes"></app-body-quote>
        <div class="row">
            <div class="col-sm-12 text-center">
                <div class="alert alert-info">Info: Click on a Quote to delete it!</div>
            </div>
        </div>

    </div>
</template>

<script>

    import QuoteGrid from "./components/QuoteGrid";
    import NewQuote from "./components/NewQuote";
    import Header from "./components/Header";

    export default {
        data: function () {
            return {
                maxQuotes: 8,
                quotes: [
                    'Vue.js is very attractive and lovely'
                ],
            }
        },
        components: {
            appBodyQuote: QuoteGrid,
            appNewQuote: NewQuote,
            appHeader: Header,
        },
        methods: {
            newQuote(quote) {

                if (this.quotes.length >= this.maxQuotes) {
                    return alert('Please delete Quotes first!');
                }
                this.quotes.push(quote);
            },
            deleteQuote(index) {
                this.quotes.splice(index, 1)
            }

        }

    }

</script>

<style>

</style>
