# 🍷 Licorería EM - Sistema Inteligente de Control y POS Serverless

🌐 **Demo en Vivo:** [Visitar Licorería EM](https://licoreria-em.netlify.app)

Un sistema de Punto de Venta (POS) ultrarrápido y gestión de inventario diseñado para resolver los desafíos de una licorería con alta rotación de productos. El sistema elimina el uso de cuadernos manuales, previniendo quiebres de stock en horarios pico (fines de semana) y calculando la ganancia neta exacta en cada transacción.

## 🏗️ Arquitectura y Decisiones Técnicas

Este proyecto está construido bajo una arquitectura **Zero-Cost Serverless**, ideal para microempresas que necesitan digitalizarse sin pagar costosas licencias, hosting dedicado o mantenimiento de servidores de bases de datos.

### ¿Por qué un único archivo `index.html`?
El frontend es una **Single Page Application (SPA)** contenida en un solo archivo que integra HTML5, CSS3 y JavaScript Vanilla.
* **Velocidad Extrema en Caja:** Al no requerir recargas de página ni depender de frameworks pesados, el cajero puede registrar ventas consecutivas en segundos, algo vital durante la alta afluencia de clientes.
* **Despliegue Inmediato:** Alojado de forma gratuita en Netlify, garantizando alta disponibilidad y actualizaciones instantáneas.

### ¿Por qué Google Sheets y Apps Script?
La persistencia de datos maneja un archivo estructurado de Google Sheets (`bd_proytic`) conectado a través de **Google Apps Script** como una API REST.
* **Backend Transparente:** Las funciones `doPost` y `doGet` automatizan la generación de IDs únicos (UUID), estampas de tiempo y el cálculo de inventario.
* **Control Total para el Propietario:** El dueño del negocio visualiza sus datos en un formato de hoja de cálculo familiar, lo que facilita realizar auditorías físicas, correcciones manuales y respaldos sin necesitar conocimientos en SQL.

## ✨ Características Principales

* ⚡ **Punto de Venta (POS) Ágil:** Selección de bebidas desde un catálogo dinámico con autocompletado de precios y cálculo en vivo del ingreso total y la ganancia estimada.
* 💰 **Cálculo Automático de Ganancia Neta:** El backend deduce el costo de compra del precio de venta en tiempo real, registrando exactamente cuánto dinero limpio genera cada transacción.
* 📦 **Gestión de Abastecimiento:** Módulo de ingresos que suma mercancía al inventario y recalcula los costos de reposición automáticamente.
* 🚨 **Monitor de Alertas y Stock:** Panel integrado que detecta productos con baja rotación o que están alcanzando niveles críticos (quiebre de stock).
* 📊 **Integración con Inteligencia de Negocios (BI):** Base de datos optimizada para conectarse directamente con **Looker Studio**, permitiendo proyectar tableros gerenciales y gráficos interactivos sin latencia.
* 🎨 **Diseño Moderno (Soft UI):** Interfaz limpia, responsiva y translúcida (Glassmorphism), adaptada ergonómicamente para su uso en tablets, celulares y computadoras de escritorio.

## 🛠️ Stack Tecnológico

**Frontend:**
* HTML5 (Semántico)
* CSS3 (Glassmorphism, Flexbox, UI/UX enfocado en POS)
* JavaScript Vanilla (Peticiones asíncronas con Fetch API)

**Backend & Datos:**
* Google Apps Script (Controlador API)
* Google Sheets (Base de Datos Relacional Ligera)
* Google Looker Studio (Visualización de Datos / Tableros)

**Hosting:**
* Netlify (Edge CDN)

## 🚀 Instalación y Uso Local

1. Clona este repositorio:
   ```bash
   git clone [https://github.com/triwot/licoreria-em.git](https://github.com/triwot/licoreria-em.git)
