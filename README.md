# Marín Digital

![Estado](https://img.shields.io/badge/estado-completo-brightgreen)
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
- **Recomendación con IA:** el usuario indica lo que necesita, su reto, su nivel y sus días de entrenamiento si aplica, y el asesor virtual sugiere el paquete que mejor encaja. La IA solo puede recomendar paquetes del catálogo real, y si no responde, la página muestra una recomendación de respaldo.
- **Descuento por combinación:** al contratar dos o más servicios como un solo paquete, se aplica un 10 % de descuento.
- **Formulario de contacto:** las solicitudes se guardan en una base de datos y quedan disponibles para el administrador.
- **Panel de administración:** acceso protegido con usuario y contraseña. Permite ver todas las solicitudes y cambiar su estado (nueva, en proceso, cerrada).
- **Diseño responsive:** adaptado a celular, tableta y computadora.

## Arquitectura

El proyecto está separado en dos partes:

```
Página (GitHub Pages)                 Backend (Render)               Servicios externos
marin-digital                         marin-backend                  
├── index.html   ── solicitudes ───▶  server.js (Node + Express) ─▶  MongoDB Atlas (base "marin")
├── admin.html   ── panel admin ───▶  /api/admin/...               Groq (recomendación con IA)
├── styles.css   ── recomendación ─▶  /api/recomendacion ─────────▶ 
└── README.md
```


Repositorio del backend: [abd-ship/marin-backend](https://github.com/abd-ship/marin-backend)

## Tecnologías

| Capa | Tecnología | Uso |
|---|---|---|
| Estructura | HTML5 | Contenido y secciones |
| Estilos | CSS3 | Diseño, tipografía y adaptación a pantallas |
| Interacción | JavaScript | Recomendación, formulario y panel admin |
| Tipografía | Google Fonts | Fraunces y Plus Jakarta Sans |
| Backend | Node.js y Express | API para solicitudes, admin e IA |
| Base de datos | MongoDB Atlas | Almacenamiento de solicitudes |
| Inteligencia artificial | Groq | Redacción de la recomendación personalizada |
| Publicación de la página | GitHub Pages | Hosting del sitio estático |
| Publicación del backend | Render | Hosting del servidor |

## Estructura del repositorio

```
marin-digital/
├── index.html    Página principal
├── styles.css    Hojas de estilo
├── admin.html    Panel de administración
└── README.md     Documentación del proyecto
```

## Autor

**Carlos Marín**
Desarrollo web · Calistenia · Marketing digital

---

© 2026 Marín Digital. Todos los derechos reservados.
