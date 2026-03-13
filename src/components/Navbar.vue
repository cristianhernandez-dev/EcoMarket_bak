<template>
  <header class="navbar">
    <div class="logo">EcoMarket</div>

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
export default {
  name: "Navbar"
}
</script>

<style scoped>
.navbar {
  background-color: #2e7d32;
  color: white;
  padding: 1rem 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  font-size: 1.3rem;
  font-weight: bold;
}

.nav-list {
  list-style: none;
  display: flex;
  gap: 1rem;
}

.nav-list a {
  color: white;
  text-decoration: none;
  font-weight: bold;
}

.nav-list a:hover {
  text-decoration: underline;
}
</style>
