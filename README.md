# Marín Digital

![Estado](https://img.shields.io/badge/estado-en%20desarrollo-yellow)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![Node.js](https://img.shields.io/badge/Node.js-339933?logo=nodedotjs&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?logo=mongodb&logoColor=white)

Sitio web de **Marín Digital**, una oferta de servicios que combina desarrollo de páginas web, asesoría personalizada de calistenia y street workout, y marketing digital.

🔗 **Sitio en producción:** [abd-ship.github.io/marin-digital](https://abd-ship.github.io/marin-digital/)

🔐 **Panel de administración:** [abd-ship.github.io/marin-digital/admin.html](https://abd-ship.github.io/marin-digital/admin.html)

---

## Servicios

| Servicio | Descripción |
|---|---|
| **Páginas web** | Landing pages responsive en tres niveles: Básica, Estándar y Premium. |
| **Calistenia y street workout** | Planes personalizados por nivel (Principiante, Intermedio, Avanzado) con evaluación inicial y seguimiento. |
| **Marketing digital** | Diagnóstico, estrategia de contenido y campañas en redes en tres niveles: Básico, Estándar y Premium. |

## Funcionalidades

- **Inicio:** acceso directo a los precios de cada servicio desde sus íconos.
- **Proceso de trabajo:** cuatro etapas, desde la reunión inicial hasta la entrega y el seguimiento.
- **Recomendación personalizada:** cuatro preguntas (servicios de interés, reto principal, nivel y días de entrenamiento si aplica, y canal de contacto) que generan una sugerencia de plan.
- **Descuento por combinación:** al contratar dos o más servicios como un solo paquete, se aplica un 10 % de descuento.
- **Formulario de contacto:** las solicitudes se guardan en una base de datos y quedan disponibles para el administrador.
- **Panel de administración:** acceso protegido con usuario y contraseña. Permite ver todas las solicitudes y cambiar su estado (nueva, en proceso, cerrada).
- **Diseño responsive:** adaptado a celular, tableta y computadora.

## Arquitectura

El proyecto está separado en dos partes:

```
Página (GitHub Pages)                 Backend (Render)              Base de datos
marin-digital                         marin-backend                 MongoDB Atlas
├── index.html   ── solicitudes ───▶  server.js (Node + Express) ─▶  base "marin"
├── admin.html   ── panel admin ───▶  /api/admin/...              colección "solicitudes"
├── styles.css
└── README.md
```

- La **página** es estática y se publica en GitHub Pages.
- El **backend** recibe las solicitudes y las guarda en MongoDB. También valida el acceso al panel admin.
- Las contraseñas y la conexión a la base viven solo en las variables de entorno de Render, nunca en el código.

Repositorio del backend: [abd-ship/marin-backend](https://github.com/abd-ship/marin-backend)

## Tecnologías

| Capa | Tecnología | Uso |
|---|---|---|
| Estructura | HTML5 | Contenido y secciones |
| Estilos | CSS3 | Diseño, tipografía y adaptación a pantallas |
| Interacción | JavaScript | Recomendación, formulario y panel admin |
| Tipografía | Google Fonts | Fraunces y Plus Jakarta Sans |
| Backend | Node.js y Express | API para solicitudes y acceso admin |
| Base de datos | MongoDB Atlas | Almacenamiento de solicitudes |
| Publicación | GitHub Pages | Hosting de la página |
| Servidor | Render | Hosting del backend |

## Estructura del repositorio

```
marin-digital/
├── index.html    Página principal
├── styles.css    Hojas de estilo
├── admin.html    Panel de administración
└── README.md     Documentación del proyecto
```

## Ejecución local

**Página:** abre `index.html` en tu navegador. Para que el formulario guarde solicitudes en tu computadora, el backend debe estar corriendo en `localhost:3000`.

**Backend:**

```bash
git clone https://github.com/abd-ship/marin-backend.git
cd marin-backend
npm install
```

Crea un archivo `.env` con estas variables (sin subirlo a GitHub):

```
MONGODB_URI=mongodb+srv://USUARIO:CONTRASEÑA@cluster0.mcvp88z.mongodb.net/
ADMIN_USER=usuario_admin
ADMIN_PASSWORD=contraseña_admin
PORT=3000
```

Después ejecuta `npm start`.

## Estado del proyecto

| Módulo | Estado |
|---|---|
| Inicio y catálogo de servicios con paquetes y precios | ✅ Completo |
| Proceso de trabajo | ✅ Completo |
| Recomendación personalizada y descuento por combinación | ✅ Completo |
| Formulario de contacto con guardado en MongoDB | ✅ Completo |
| Publicación de la página en GitHub Pages | ✅ Completo |
| Backend con Node.js y Express en Render | ✅ Completo |
| Panel de administración con login y gestión de estados | ✅ Completo |
| IA aplicada en la recomendación | 📋 Planeado |
| Revisión final y preparación de la defensa | 📋 Planeado |

---

## Autor

**Carlos Marín**
Desarrollo web · Calistenia · Marketing digital

---

© 2026 Marín Digital. Todos los derechos reservados.
