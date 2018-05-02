<template>
    <div class="container">
        <appQuoteGrid :quotes="quotes">
        </appQuoteGrid>
    </div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue';
export default {
  data: function() {
    return {
      quotes: ['Just a quote to see something', 'quote 2', 'quote 3'],
      maxQuotes: 10
    };
  },
  components: {
    appQuoteGrid: QuoteGrid
  }
};
</script>

<style>

</style>
