<template>
  <section class="product-list">
    <ProductCard
      v-for="producto in productos"
      :key="producto.id"
      :nombre="producto.nombre"
      :precio="producto.precio"
      :imagen="producto.imagen"
      :disponible="producto.disponible"
      @agregar-carrito="$emit('agregar-carrito')"
    />
  </section>
</template>

<script>
import ProductCard from './ProductCard.vue'

export default {
  name: 'ProductList',
  components: {
    ProductCard
  },
  props: {
    productos: Array
  }
}
</script>

<style scoped>
.product-list {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 1rem;
  margin-top: 1.5rem;
}
</style>
