<template>
  <div class="col-md-4">
    <div class="card card-body mb-4 animate__animated" :class="{animate__headShake: isHovering}" @mouseover="isHovering = true" @mouseout="isHovering = false">
      <slot></slot>
    </div>
  </div>  
</template>

<script>
export default {
  data() {
    return {
      isHovering: false
    }
  }
}
</script>

<style scoped>
  .card {
    font-family: 'Sacramento', 'Roboto', Arial, Helvetica, sans-serif;
    transition: all ease-in-out 150ms;
    font-size: 1.75rem;
  }

  .card:hover {
    background-color: #E3655B;
    color: #FFFFFF;
    cursor: pointer;
    animation-delay: 400ms;
  }
</style>
