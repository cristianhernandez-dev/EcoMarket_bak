<template>
  <div class="app">

    <Navbar />

    <main class="main-content" id="inicio">

      <h1>Tienda Online</h1>

      <CardContainer>
        <h2>Productos destacados</h2>
        <p>
          Explora nuestra selección de productos responsables con el medioambiente.
        </p>
      </CardContainer>

      <section id="productos">
        <ProductList
          :productos="productos"
          @agregar-carrito="agregarAlCarrito"
        />
      </section>

      <p class="cart-message" id="carrito">
        Productos en carrito: {{ carrito }}
      </p>

      <p v-if="mensaje" class="success-message">
        {{ mensaje }}
      </p>

      <section id="contacto" class="contact-section">
        <h2>Contacto</h2>
        <p>
          Escríbenos para conocer más sobre nuestros productos ecológicos.
        </p>
      </section>

    </main>

    <Footer />

  </div>
</template>

<script>

import Navbar from './components/Navbar.vue'
import ProductList from './components/ProductList.vue'
import CardContainer from './components/CardContainer.vue'
import Footer from './components/Footer.vue'

import cepillo from './assets/images/cepillo-bambu.jpeg'
import botella from './assets/images/botella-reutilizable.jpeg'
import bolsa from './assets/images/bolsa-ecologica.webp'

export default {
  name: 'App',

  components: {
    Navbar,
    ProductList,
    CardContainer,
    Footer
  },

  data() {
    return {

      carrito: 0,

      mensaje: '',
productos: [
  {
    id: 1,
    nombre: 'Cepillo de bambú',
    precio: 3990,
    imagen: cepillo,
    disponible: true
  },
  {
    id: 2,
    nombre: 'Botella reutilizable',
    precio: 7990,
    imagen: botella,
    disponible: true
  },
  {
    id: 3,
    nombre: 'Bolsa ecológica',
    precio: 2990,
    imagen: bolsa,
    disponible: false
  }
]

    }
  },

  methods: {

    agregarAlCarrito() {

      this.carrito++

      this.mensaje = "Producto agregado al carrito"

      setTimeout(() => {
        this.mensaje = ''
      }, 2000)

    }

  },

  created() {
    console.log("Aplicación creada")
  },

  mounted() {
    console.log("Aplicación montada en el DOM")
  }

}
</script>

<style scoped>

.main-content {
  max-width: 1100px;
  margin: 0 auto;
  padding: 2rem 1rem;
}

h1 {
  margin-bottom: 0.5rem;
  color: #2e7d32;
}

.subtitle {
  margin-bottom: 1.5rem;
  color: #555;
}

.cart-message {
  margin-top: 1.5rem;
  font-weight: bold;
  color: #1b5e20;
}

.success-message {
  margin-top: 0.8rem;
  color: #2e7d32;
  font-weight: bold;
}

.contact-section {
  margin-top: 2rem;
}

</style>
