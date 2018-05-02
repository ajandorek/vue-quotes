<template>
    <div class="container">
        <appNewQuote @quoteAdded="newQuote"></appNewQuote>
        <appQuoteGrid :quotes="quotes" @quoteDeleted="deleteQuote">
        </appQuoteGrid>
        <div class="col-sm-12 text-center">
          <div class="alert alert-info">Click on a Quote to delete it!</div>
        </div>
    </div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue';
import NewQuote from './components/NewQuote.vue';
export default {
  data: function() {
    return {
      quotes: ['Just a quote to see something'],
      maxQuotes: 10
    };
  },
  methods: {
    newQuote(quote) {
      this.quotes.push(quote);
    },
    deleteQuote(i) {
      this.quotes.splice(i, 1);
    }
  },
  components: {
    appQuoteGrid: QuoteGrid,
    appNewQuote: NewQuote
  }
};
</script>

<style>

</style>
