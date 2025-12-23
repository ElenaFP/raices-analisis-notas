# Análisis de Notas - Raíces

Este proyecto es una aplicación web portable (Single Page Application) diseñada para analizar las calificaciones de los alumnos exportadas desde la plataforma **Raíces**.

La herramienta permite visualizar estadísticas de aprobados y suspensos por grupo, así como agrupar unidades (clases) de forma dinámica.

🔗 **[Ver aplicación desplegada](https://elenafp.github.io/raices-analisis-notas/)**

## 🚀 Características

*   **Privacidad total:** Todo el procesamiento se realiza en tu navegador. **Ningún dato se sube a ningún servidor.**
*   **Portable:** Un único fichero `.html` que funciona sin internet.
*   **Análisis Automático:**
    *   Detecta grupos y alumnos automáticamente desde el CSV.
    *   Filtra asignaturas matriculadas (ignora pendientes/convalidadas).
    *   Deduplica materias para evitar conteos erróneos.
*   **Agrupación Dinámica:** Permite unir varios grupos (ej. "1A", "1B" -> "1º ESO") para ver estadísticas conjuntas.
*   **Visualización Clara:** Tabla de resultados con código de colores para identificar rápidamente situaciones críticas.

## 📋 Cómo usarlo

1.  **Exporta tus datos:** Obtén el fichero CSV de calificaciones desde Raíces.
2.  **Abre la aplicación:**
    *   Si la usas online: Accede a [https://elenafp.github.io/raices-analisis-notas/](https://elenafp.github.io/raices-analisis-notas/)
    *   Si la usas local: Abre el archivo `index.html` en tu navegador (Chrome, Edge, Firefox, etc.).
3.  **Carga el fichero:** Arrastra el archivo `.csv` al recuadro punteado.
4.  **Analiza:**
    *   Verás inmediatamente la tabla de resultados por grupo original.
    *   Pulsa en **"⚙️ Agrupar Unidades"** para combinar clases.
    *   Selecciona las clases, escribe un nombre nuevo y pulsa "Agrupar".

## 🛠️ Tecnologías

*   HTML5
*   CSS3
*   JavaScript (ES6+)
*   FileReader API para lectura local de archivos.

## 📦 Despliegue en GitHub Pages

Este proyecto está configurado para desplegarse automáticamente en GitHub Pages.
Simplemente sube el archivo `index.html` a la rama `main` de tu repositorio y activa GitHub Pages en la configuración.

1.  Ve a `Settings` > `Pages`.
2.  En `Source`, selecciona `Deploy from a branch`.
3.  En `Branch`, selecciona `main` y la carpeta `/ (root)`.
4.  Guarda los cambios.
