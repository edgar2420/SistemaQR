# SistemaQR
Gestor web para generar, imprimir y escanear códigos QR asociados a ítems (equipos, productos, documentos o personas), con historial de escaneos, control de usuarios y roles, búsquedas y reportes.
## Objetivos
* Etiquetar activos con QR y vincularlos a su ficha.
* Consultar/actualizar información rápida mediante escaneo.
* Trazar movimientos y auditoría con un historial de escaneos.
* Permitir diferentes permisos por rol (ADMIN / OPERADOR).
## Tecnologías Utilizadas
* Frontend: React + TypeScript, Vite, React Router, Axios, Tailwind.
* Backend: Node.js + Express (Arquitectura Limpia).
* DB: PostgreSQL (consulta SQL directa o mediante ORM ligero).
* Tests: Vitest/Jest, Supertest (API), Cypress.
## Dependencias útiles
### Frontend
npm i react-router-dom axios @zxing/library <br>
npm i -D tailwindcss postcss autoprefixer
## Flujos clave del Front
* Listado de ítems con filtros y paginación.
* Creación/Edición con validación y previsualización de QR.
* Impresión masiva: generar “planilla” A4 con múltiples QR.
* Escaneo: <br> * Cámara del navegador → decodifica QR → navega a /items/:codigo o llama /api/q/:codigo. <br> * Si sin cámara (desktop), input manual del codigo.

