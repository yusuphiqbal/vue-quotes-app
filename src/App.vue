<template>
  <div class="container">
    <div class="row">
      <div class="col mb-5">
        <app-header :quoteCount="quotes.length" :maxQuotes="maxQuotes"></app-header>
      </div>
    </div>
    <div class="row mb-5">
      <div class="col">
        <app-new-quote @quoteAdded="newQuote"></app-new-quote>
      </div>
    </div>
    <div class="row">
      <div class="col">
        <div class="alert alert-info mb-4">
          <span>Click on a quote to delete</span>
        </div>
        <app-quote-grid :quotes="quotes" @quoteDeleted="deleteQuote"></app-quote-grid>
      </div>
    </div>
  </div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue'
import NewQuote from './components/NewQuote'
import Header from './components/Header'

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
    appQuoteGrid: QuoteGrid,
    appNewQuote: NewQuote,
    appHeader: Header
  },
  methods: {
    newQuote(quote) {
      if (this.quotes.length >= this.maxQuotes) {
        return alert('Delete quotes first.')
      }
      this.quotes.push(quote)
    },
    deleteQuote(index) {
      this.quotes.splice(index, 1)
    }
  }
}
</script>

<style>
  .container {
    font-family: 'Roboto', Arial, Helvetica, sans-serif;
  }
</style>
