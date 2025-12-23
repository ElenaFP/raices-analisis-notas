# Contexto de la Sesión

**Fecha:** 23 de Diciembre de 2025  
**Objetivo:** Crear una aplicación web portable (Single Page Application) para el análisis de notas de alumnos a partir de un fichero CSV de Raíces.

## Ficheros de Trabajo
- **Directorio:** `C:\Users\elena\Desktop\aprobados`
- **Fichero Principal:** `index.html` (Aplicación web)
- **Documentación:** `README.md`
- **Configuración CI/CD:** `.github/workflows/deploy.yml`
- **Fichero de datos:** `DescargaExpGesExpDat_20251223_164900_105367.CSV`

## Estado del Proyecto
🚀 **Desplegado y Funcional.** La aplicación está en GitHub Pages y cuenta con lógica avanzada de análisis.

### Funcionalidades Implementadas
1.  **Lectura Local:** Sistema Drag & Drop para procesar CSVs sin salida de datos del cliente (privacidad total).
2.  **Lógica de Negocio Educativa:**
    - **Filtros:** Solo alumnos con estado "Matriculada".
    - **Deduplicación:** Gestión de duplicados en la columna `MATERIA_GENERAL`.
    - **Normalización de Notas:** Soporte para sufijos de Matrícula de Honor (`-M`) y gestión de decimales con coma.
    - **Evaluación Final Inteligente:** Selección automática entre `NOTAORD` y `EVFINAL(LOMLOE)`.
3.  **Interfaz de Usuario (UX/UI):**
    - **Pestañas:** Organización de resultados por evaluaciones (1ª, 2ª, Final y Extraordinaria).
    - **Dinámica:** La tabla extraordinaria solo aparece si hay datos reales.
    - **Agrupación de Unidades:** Interfaz protegida para renombrar y combinar grupos de forma masiva.
    - **Contexto:** Extracción y muestra del año académico (`C_ANNO`).
4.  **Infraestructura:**
    - Despliegue automático mediante **GitHub Actions**.
    - Configuración de `README.md` para el repositorio de ElenaFP.
    - `.gitignore` configurado para proteger la privacidad de los datos reales.

## Historial de Cambios (Resumen)
- Implementación inicial de tabla de aprobados.
- Añadido sistema de agrupación de unidades.
- Incorporación de múltiples evaluaciones (1ª, 2ª, Final).
- Refuerzo de parsing para casos especiales (Matrículas de Honor).
- Cambio a diseño basado en pestañas para mejorar la usabilidad.