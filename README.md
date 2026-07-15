# 🎟️ Sorteo Transparente

Aplicación web que valida participantes de sorteos de Instagram y realiza un sorteo **justo, reproducible y auditable**, eliminando las limitaciones de las herramientas tradicionales.

---

## 🚀 ¿Por qué nació este proyecto?

Mientras organizaba un sorteo para mi emprendimiento **Caserito Bakery**, descubrí que varias aplicaciones populares solo procesaban los primeros **100 comentarios** de una publicación.

Como el post tenía más de **150 comentarios**, una gran parte de los participantes quedaba automáticamente excluida del sorteo.

En lugar de aceptar esa limitación, desarrollé una herramienta propia capaz de procesar todos los comentarios y generar un sorteo transparente.

---

## ✨ Características

- 📂 Procesa archivos **CSV** y **Excel**.
- 🔍 Detecta automáticamente las columnas de usuario y comentario.
- ✅ Valida reglas de participación (por ejemplo, mencionar a otro usuario).
- 🚫 Elimina participaciones duplicadas.
- 🎲 Realiza el sorteo utilizando el algoritmo **Fisher-Yates Shuffle**.
- 🏆 Selecciona ganador y suplentes.
- 📄 Genera un archivo de auditoría con toda la información del sorteo.
- 💻 Funciona completamente en el navegador, sin necesidad de backend.

---

## ⚙️ ¿Cómo funciona?

### 1. Extracción de comentarios

Los comentarios se obtienen a partir del HTML renderizado de una publicación de Instagram utilizando **Python** y **BeautifulSoup**, evitando las limitaciones de otras herramientas.

### 2. Validación de participaciones

La aplicación analiza el archivo generado y verifica automáticamente que cada participación cumpla las reglas del sorteo:

- Mención válida a otro usuario.
- Una única participación por persona.
- Exclusión automática de registros inválidos.

### 3. Sorteo

Con el conjunto de participantes válidos se ejecuta un **Fisher-Yates Shuffle**, garantizando una distribución aleatoria uniforme para seleccionar al ganador y los suplentes.

### 4. Auditoría

Al finalizar el proceso se genera un archivo de respaldo con:

- Fecha del sorteo.
- Semilla utilizada.
- Lista completa de participantes válidos.
- Ganador.
- Suplentes.

Esto permite que cualquier persona pueda verificar posteriormente cómo se realizó el sorteo.

---

## 🛠️ Tecnologías utilizadas

### Frontend

- HTML5
- CSS3
- JavaScript (Vanilla)

### Procesamiento de archivos

- SheetJS

### Extracción de datos

- Python
- BeautifulSoup

### Algoritmos

- Fisher-Yates Shuffle

---

## 📊 Caso de uso real

Este proyecto fue desarrollado para realizar un sorteo de **Caserito Bakery**, un emprendimiento de galletas artesanales.

### Resultados

- 💬 182 comentarios procesados.
- ✅ 19 participaciones válidas luego de aplicar las reglas del sorteo.
- 🏆 1 ganador + 2 suplentes seleccionados.
- 📄 Registro auditable generado automáticamente.

---

## 📚 Aprendizajes

Durante el desarrollo de este proyecto trabajé en:

- Limpieza y validación de datos.
- Automatización de reglas de negocio.
- Procesamiento de archivos CSV y Excel.
- Manipulación del DOM y procesamiento de datos con JavaScript.
- Extracción de información mediante Python y BeautifulSoup.
- Implementación de algoritmos de aleatoriedad.
- Diseño de una aplicación completamente funcional sin backend.

---

## 🎯 Objetivo

El objetivo principal fue construir una herramienta que permitiera realizar sorteos de Instagram de manera **transparente, verificable y sin restricciones arbitrarias**, ofreciendo una solución real a un problema encontrado durante la organización de un sorteo.
