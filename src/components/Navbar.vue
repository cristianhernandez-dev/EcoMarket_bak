<template>
  <header class="navbar">

    <div class="logo">
      <img :src="logo" alt="EcoMarket Logo">
      <span>Productos ecológicos y sostenibles</span>
    </div>

    <nav>
      <ul class="nav-list">
        <li><a href="#inicio">Inicio</a></li>
        <li><a href="#productos">Productos</a></li>
        <li><a href="#contacto">Contacto</a></li>
        <li><a href="#carrito">Carrito</a></li>
      </ul>
    </nav>

  </header>
</template>

<script>
import logo from '../assets/images/logo-ecomarket.png'


export default {
  name: "Navbar",
  data() {
    return { logo }
  }
}
</script>

<style scoped>
.navbar {
  background-color: #2e7d32;
  color: white;
  padding: 1rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo img {
  height: 60px;
  border-radius: 3px;
}


.nav-list {
  list-style: none;
  display: flex;
  gap: 1rem;
}

.nav-list a {
  color: white;
  text-decoration: none;
}
</style>