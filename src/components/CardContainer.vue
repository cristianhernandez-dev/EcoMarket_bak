<template>
  <div class="card-container">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'CardContainer'
}
</script>

<style scoped>
.card-container {
  background-color: #e8f5e9;
  border-left: 6px solid #43a047;
  padding: 1rem;
  border-radius: 10px;
  margin-bottom: 1.5rem;
}
</style>
