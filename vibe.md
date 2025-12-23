# Contexto de la Sesión

**Fecha:** 23 de Diciembre de 2025  
**Objetivo:** Crear una aplicación web portable (Single Page Application) para el análisis de notas de alumnos a partir de un fichero CSV de Raíces.

## Ficheros de Trabajo
- **Directorio:** `C:\Users\elena\Desktop\aprobados`
- **Fichero Principal:** `index.html` (Aplicación web)
- **Documentación:** `README.md`
- **Configuración CI/CD:** `.github/workflows/deploy.yml`
- **Fichero de datos:** `DescargaExpGesExpDat_*.CSV`

## Estado del Proyecto
🚀 **Desplegado y Funcional.** La aplicación está en GitHub Pages con una interfaz moderna y unificada con el proyecto de asistencia.

### Funcionalidades Implementadas
1.  **Privacidad y Seguridad:** Procesamiento 100% local en el navegador. Los datos nunca se suben a ningún servidor (RGPD compatible).
2.  **Lógica de Negocio Educativa:**
    - **Filtros:** Solo alumnos con estado "Matriculada".
    - **Deduplicación:** Gestión de duplicados en la columna `MATERIA_GENERAL`.
    - **Normalización de Notas:** Soporte para sufijos de Matrícula de Honor (`-M`) y gestión de decimales con coma/punto.
    - **Evaluación Final Inteligente:** Selección automática entre `NOTAORD` y `EVFINAL(LOMLOE)`.
3.  **Interfaz de Usuario (UX/UI):**
    - **Diseño Unificado:** Estilo visual (colores, fuentes, sombras) sincronizado con `raices-analisis-asistencia`.
    - **Pestañas:** Organización de resultados por evaluaciones (1ª, 2ª, Final y Extraordinaria).
    - **Persistencia:** La zona de carga (Drag & Drop) permanece visible para facilitar el análisis de múltiples archivos.
    - **Agrupación de Unidades:** Interfaz mejorada para renombrar y combinar grupos (ej. unir letras en un solo nivel).
4.  **Exportación de Datos:**
    - Botones de descarga CSV en cada tabla de resultados.
    - Generación dinámica de nombres de archivo incluyendo el año académico.
5.  **Infraestructura:**
    - Despliegue automático mediante **GitHub Actions**.
    - Documentación completa en `README.md` incluyendo guía de exportación de Raíces.

## Historial de Cambios (Resumen)
- Implementación inicial de tabla de aprobados.
- Añadido sistema de agrupación de unidades.
- Incorporación de múltiples evaluaciones (1ª, 2ª, Final).
- Refuerzo de parsing para casos especiales (Matrículas de Honor).
- **Unificación de Interfaz:** Aplicado el estilo visual del proyecto de asistencia para coherencia de marca.
- **Descarga CSV:** Añadida funcionalidad para exportar los resultados calculados desde cada pestaña.
- **Mejora de UX:** Corregida la desaparición del área de carga tras procesar un archivo.
- **Documentación:** README.md reescrito con enfoque en seguridad y tutorial de uso.
