<template>
  <div class="row">
    <div class="col">
      <form>
        <div class="form-group">
          <label>Quote</label>
          <textarea class="form-control" rows="3" v-model="quote"></textarea>
        </div>
        <button class="btn btn-primary" @click.prevent="createNew">Add Quote</button>
      </form>
    </div>
  </div>  
</template>

<script>
export default {
  data() {
    return {
      quote: ''
    }
  },
  methods: {
    createNew() {
      this.$emit('quoteAdded', this.quote)
      this.quote = ''
    }
  }
}
</script>

<style>

</style>
