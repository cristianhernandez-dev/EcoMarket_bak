
# 🌱 EcoMarket – Aplicación Vue con Componentización

Aplicación web desarrollada con **Vue 3** que simula una tienda online de productos ecológicos y sostenibles.
El proyecto demuestra la implementación de **componentes reutilizables**, comunicación entre componentes y uso del **ciclo de vida de Vue**.

Este proyecto fue desarrollado como parte del módulo:

**Desarrollo de aplicaciones front-end con framework Vue**

---

# 📌 Objetivos del proyecto

El proyecto busca aplicar los siguientes conceptos de Vue:

- Componentización de la interfaz
- Arquitectura modular
- Comunicación entre componentes
- Uso de props
- Emisión de eventos con `$emit`
- Uso de slots
- Hooks del ciclo de vida
- Aplicación de estilos dinámicos

---

# 🧰 Tecnologías utilizadas

| Tecnología | Uso |
|------------|-----|
| Vue 3 | Framework principal |
| Vite | Herramienta de desarrollo |
| JavaScript | Lógica de la aplicación |
| HTML5 | Estructura de la interfaz |
| CSS3 | Estilos de la aplicación |

---

# 📂 Estructura del proyecto

```
EcoMarket
│
├── index.html
├── package.json
├── vite.config.js
│
├── src
│   ├── main.js
│   ├── App.vue
│   │
│   ├── assets
│   │   ├── styles.css
│   │   └── images
│   │        ├── cepillo-bambu.jpg
│   │        ├── botella-reutilizable.jpg
│   │        └── bolsa-ecologica.jpg
│   │
│   └── components
│       ├── Navbar.vue
│       ├── ProductList.vue
│       ├── ProductCard.vue
│       ├── CardContainer.vue
│       └── Footer.vue
```

---

# 🧩 Jerarquía de componentes

```
App.vue
│
├── Navbar.vue
├── CardContainer.vue
├── ProductList.vue
│     └── ProductCard.vue
└── Footer.vue
```

### Descripción de componentes

**App.vue**

Componente principal que gestiona:

- estado del carrito
- listado de productos
- comunicación entre componentes

**Navbar.vue**

Barra de navegación principal de la aplicación.

**ProductList.vue**

Componente encargado de mostrar la lista de productos utilizando iteración (`v-for`).

**ProductCard.vue**

Representa cada producto individual incluyendo:

- imagen
- nombre
- precio
- estado de disponibilidad
- botón para agregar al carrito

**CardContainer.vue**

Componente reutilizable que utiliza **slots** para insertar contenido dinámico.

**Footer.vue**

Pie de página de la aplicación.

---

# ⚙️ Funcionalidades implementadas

✔ Visualización de productos ecológicos  
✔ Componentes reutilizables  
✔ Comunicación entre componentes mediante **props**  
✔ Eventos personalizados utilizando **$emit**  
✔ Uso de **slots** para contenido dinámico  
✔ Contador de productos agregados al carrito  
✔ Estilos dinámicos usando **class binding** y **style binding**

---

# 🔄 Hooks del ciclo de vida utilizados

En el componente principal se utilizan los siguientes hooks:

### `created()`

Se ejecuta cuando el componente es creado y permite inicializar lógica o cargar datos.

### `mounted()`

Se ejecuta cuando el componente ya se encuentra montado en el DOM.

---

# 🚀 Instalación del proyecto

Para ejecutar el proyecto en un entorno local:

### 1️⃣ Instalar dependencias

```
npm install
```

### 2️⃣ Ejecutar el servidor de desarrollo

```
npm run dev
```

La aplicación estará disponible en:

```
http://localhost:5173
```

---

# 🖥 Captura de la aplicación

Aquí puedes agregar una captura del proyecto funcionando.

---

# 👨‍💻 Autor

Proyecto desarrollado por:

**Cristián Hernández**

Curso: Desarrollo de aplicaciones front-end con Vue
