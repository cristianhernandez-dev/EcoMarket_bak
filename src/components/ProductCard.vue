<template>
  <div
    class="product-card"
    :class="{ agotado: !disponible }"
    :style="{ borderColor: disponible ? '#4caf50' : '#e53935' }"
  >
    <img :src="imagen" :alt="nombre" />
    <h3>{{ nombre }}</h3>
    <p class="price">${{ precio }}</p>
    <p>{{ disponible ? 'Disponible' : 'Agotado' }}</p>

    <button
      @click="agregar"
      :disabled="!disponible"
    >
      Agregar al carrito
    </button>
  </div>
</template>

<script>
export default {
  name: 'ProductCard',
  props: {
    nombre: String,
    precio: Number,
    imagen: String,
    disponible: Boolean
  },
  methods: {
    agregar() {
      this.$emit('agregar-carrito')
    }
  }
}
</script>

<style scoped>
.product-card {
  background: white;
  border: 2px solid;
  border-radius: 12px;
  padding: 1rem;
  text-align: center;
  transition: 0.3s ease;
}

.product-card img {
  border-radius: 8px;
  margin-bottom: 1rem;
}

.price {
  font-weight: bold;
  color: #2e7d32;
  margin: 0.5rem 0;
}

button {
  margin-top: 0.8rem;
  background-color: #43a047;
  color: white;
  border: none;
  padding: 0.7rem 1rem;
  border-radius: 8px;
}

button:disabled {
  background-color: #bdbdbd;
  cursor: not-allowed;
}

.agotado {
  opacity: 0.7;
}
</style>
