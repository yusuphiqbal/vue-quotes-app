<template>
  <div class="col-md-4">
    <div class="card card-body">
      <slot></slot>
    </div>
  </div>  
</template>

<script>

</script>

<style scoped>
  .card {
    font-family: 'Sacramento', 'Roboto', Arial, Helvetica, sans-serif;
    transition: all 150ms ease-in-out;
    font-size: 1.75rem;
  }

  .card:hover {
    background-color: #E3655B;
    color: #FFFFFF;
    cursor: pointer;
  }
</style>
