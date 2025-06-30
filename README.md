# ExamenFinal-AplicacionesWeb
# 🍣 Sushi Orders Web App

Aplicación Web para la gestión integral de pedidos de un restaurante de sushi, construida desde cero con **Vanilla JavaScript**, **HTML**, **CSS** y **Node.js**, y migrada a **React** en una segunda etapa.

## 🗂️ Estructura del Proyecto


---

## 📐 Justificación de Patrones de Diseño

### 🔸 Frontend (Vanilla JS)

| Patrón | Archivo | Pseudocódigo | Justificación |
|-------|---------|--------------|----------------|
| **Módulo** | `/scripts/cart.js` | `const CartModule = (() => { ... })()` | Encapsula lógica de carrito de forma reusable |
| **Observer** | `/scripts/eventBus.js` | `eventBus.subscribe(), eventBus.publish()` | Sincroniza vistas como menú ↔ carrito |
| **Constructor** | `/scripts/components.js` | `function Card(data) { ... }` | Crea tarjetas de productos dinámicamente |
| **Fachada** | `/scripts/apiFacade.js` | `api.get(endpoint), api.post()` | Simplifica llamadas a la API backend |

### 🔸 Backend (Node.js)

| Patrón | Archivo | Pseudocódigo | Justificación |
|-------|---------|--------------|----------------|
| **MVC** | `routes/`, `controllers/`, `models/` | `controller.getAll = (req, res) => model.find()` | Separación clara de responsabilidades |
| **Repositorio** | `models/userRepository.js` | `UserRepository.getByEmail(email)` | Abstracción de lógica de acceso a datos |
| **JWT Auth** | `middleware/auth.js` | `verifyToken(token)` | Manejo de sesiones seguras |
| **Service Layer** | `services/bookingService.js` | `BookingService.create(data)` | Lógica de negocio separada del controlador |

---

## 🧱 Diagrama de Base de Datos

![DB Schema](schema_design/db_schema.png)

**Entidades:**
- `Usuarios(id, nombre, correo, contraseña_hash)`
- `Productos(id, nombre, descripcion, precio, categoria)`
- `Pedidos(id, usuario_id, fecha, estado)`
- `DetallesPedido(id, pedido_id, producto_id, cantidad)`
- `Reservas(id, nombre, telefono, fecha, hora, comensales)`
- `Blogs(id, autor_id, titulo, contenido, fecha)`
- `Likes(id, blog_id, usuario_id)`

---

## 📝 Documentación del Proyecto

### Funcionalidades principales:
- 🏠 Frontpage: presentación del restaurante y navegación
- 🍱 Menú interactivo con filtros y carrito de compras
- 🛒 Carrito con suma dinámica y edición
- 📅 Gestión de reservas
- 🧑 Registro, inicio de sesión y autorización
- ✍️ Blog con likes, creación y gestión de posts
- 📍 Página de contacto con mapa embebido
- 📖 Página estática "Nosotros"

### Responsividad
- Todas las vistas diseñadas para **desktop**

---

## 🚀 Pasos para Desplegar

1. **Clona el repositorio:**
   ```bash
   git clone git@github.com:usuario/sushi-orders-app.git
   cd sushi-orders-app


