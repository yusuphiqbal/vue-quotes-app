<template>
  <div>
    <h3>Quotes Added</h3>
    <div class="progress">
      <div class="progress-bar" role="progressbar" :style="{width: (quoteCount / maxQuotes) * 100 + '%'}" aria-valuenow="75" aria-valuemin="0" aria-valuemax="100"></div>
    </div>
    <h5 class="mt-3">{{ quoteCount }} / {{ maxQuotes }}</h5>
  </div>  
</template>

<script>
export default {
  props: ['quoteCount', 'maxQuotes']
}
</script>
