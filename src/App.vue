<template>
  <div class="container">
    <app-quote-grid :quotes="quotes"></app-quote-grid>
  </div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue'

export default {
  data() {
    return {
      quotes: [
        'Design is not just what it looks like and feels like. Design is how it works.'
      ],
      maxQuotes: 10
    }
  },
  components: {
    appQuoteGrid: QuoteGrid
  }
}
</script>

<style>

</style>
