# AGENTS.md

Este archivo define la estructura de agentes de IA, sus roles, las preguntas de control de calidad y la hoja de ruta paso a paso para que **Stitch** genere el código modular, responsive, limpio y accesible para **todas las pantallas** de la aplicación web **"En tus zapatos"**.

---

## 1. Visión General del Proyecto

El objetivo central es interpretar los lineamientos definidos en `Design.md` para construir una aplicación web interactiva que fomente la empatía familiar mediante una ruleta de escenarios aleatorios.

### Requisitos Innegociables:
1. **Identidad de Marca y Estética:** Uso estricto de los tokens CSS de cada rol, tipografías (`Fredoka` para títulos y `Mukta Mahee` para cuerpo), esquinas redondeadas (`24px`), sombras con elevación y textura/patrón de huellas de fondo.
2. **Estrategia Responsive:** Enfoque *Mobile-first* con diseño adaptativo probado en breakpoints: `320px`, `768px`, `1024px` y `1440px`.
3. **Accesibilidad Universal (WCAG AA):** Ratios de contraste adecuados en texto, áreas táctiles/clickeables mínimas de `44px × 44px`, estados visibles de foco y soporte ARIA para la ruleta interactiva.

---

## 2. Roles de Agentes y Matriz de Preguntas de Control

### 🎨 Agente 1: Guardián del Sistema de Diseño y UI/UX
**Objetivo:** Asegurar que el código generado por Stitch traduzca con total precisión el sistema visual y la jerarquía de diseño.

#### Preguntas de Control:
* **Tokens y Color:** ¿Se están utilizando las variables CSS nativas (`:root`) definidas para cada rol (`--color-mom: #4F0377`, `--color-dad: #1D3E89`, `--color-daughter: #AE00BC`, `--color-son: #00A0A0`, `--color-pet: #AD7E40`, `--color-grandfather: #B6BA6A`)?
* **Tipografía:** ¿Los encabezados (H1–H4) usan la tipografía **Fredoka** y los párrafos/cuerpo emplean **Mukta Mahee** con los tamaños y alturas de línea correctos?
* **Componentes y Elevación:** Las tarjetas, botones flotantes (FAB) y badges conservan sus radios de borde (`24px` / `100px`) y sombras con elevación suave
* **Adaptabilidad:** El layout ajusta sus proporciones correctamente según el sistema espacial de 8px (y sub-grilla de 4px)

---

### 💻 Agente 2: Arquitecto y Desarrollador Frontend Senior
**Objetivo:** Desarrollar componentes interactivos limpios, reutilizables y la lógica funcional del frontend.

#### Preguntas de Control:
* **Lógica de la Ruleta:** El componente de la ruleta gira de forma fluida usando animaciones/transiciones CSS (`cubic-bezier`) y selecciona un rol/escenario de manera aleatoria
* **Estados de Componentes:** Todos los botones, campos de texto y tarjetas cuentan con sus 5 estados desarrollados (`default`, `hover`, `active`, `focus` y `disabled`)
* **Layouts Responsive:** La vista móvil apila el contenido verticalmente mientras que las pantallas de escritorio (`1024px+`) distribuyen la ruleta y la tarjeta de contenido en 2 columnas
* **Estructura del Código:** El código generado es semántico (HTML5), modular y fácil de integrar en React, Vue o HTML/JS según el entorno de Stitch

---

### ♿ Agente 3: Especialista en Accesibilidad (a11y) y Rendimiento
**Objetivo:** Garantizar la usabilidad universal y el cumplimiento estricto de la norma WCAG AA.

#### Preguntas de Control:
* **Contraste Dinámico:** El texto sobre badges o fondos claros (Hijo, Mascota, Abuelo) conmuta automáticamente a texto oscuro (`#000000` o `#1A200C`) para asegurar una legibilidad de al menos 4.5:1
* **Target Táctil:** Todos los botones interactivos, opciones del menú y sectores de la ruleta cumplen con la superficie mínima de click de `44px × 44px`
* **Lectores de Pantalla:** La ruleta cuenta con `role="region"`, `aria-live="polite"` y etiquetas `aria-label` para anunciar dinámicamente el resultado al usuario
* **Movimiento Reducido:** Se incluye `@media (prefers-reduced-motion: reduce)` para reemplazar las animaciones rápidas de giro por una transición de desvanecimiento suave (*fade*)

---

### 🧠 Agente 4: Estratega de Contenido y Empatía
**Objetivo:** Velar por que la voz de la app se mantenga humana, empática, clara y adecuada para usuarios de todas las edades.

#### Preguntas de Control:
* **Narrativa:** Los títulos y párrafos narrativos explican la situación con un tono comprensivo y libre de juicios
* **Legibilidad:** La longitud de línea en las tarjetas narrativas no excede los 60–70 caracteres para facilitar la lectura en cualquier dispositivo

---

## 3. Plan de Generación de Pantallas para Stitch

Stitch debe generar el código para cada pantalla cargada 