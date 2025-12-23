# 📊 Análisis de Notas por Grupo

Herramienta web para analizar las calificaciones de alumnos por evaluaciones y grupos. Diseñada específicamente para centros educativos que usan el sistema **Raíces**.

## 🎯 ¿Qué hace esta herramienta?

Procesa los datos de calificaciones exportados desde Raíces y genera estadísticas detalladas por grupo:

- **Estadísticas de aprobados y suspensos** (Todo aprobado, 1, 2, 3 o 4+ suspensos)
- **Resultados por evaluación** (1ª, 2ª, Final Ordinaria y Extraordinaria)
- **Agrupación dinámica de unidades** (ej. unir A, B y C en "1º ESO")
- **Exportación a CSV** de los resultados calculados

## 🔒 Privacidad y Seguridad

### ✅ Tus datos NUNCA salen de tu ordenador

Esta aplicación funciona **100% en tu navegador (client-side)**:

- ❌ **NO sube archivos** a ningún servidor
- ❌ **NO almacena datos** en ninguna base de datos
- ❌ **NO envía información** por internet
- ✅ **Procesamiento local**: Todo el análisis se hace en tu navegador
- ✅ **Privacidad total**: Los datos de tus alumnos están seguros
- ✅ **RGPD/LOPD compatible**: No hay transmisión de datos personales

Una vez cargada la página web, puedes **desconectar internet** y seguirá funcionando perfectamente.

## 🚀 Cómo usar

### Paso 1: Obtener los datos desde Raíces

Para exportar las calificaciones desde el sistema Raíces:

1. Accede a **Raíces** con tus credenciales
2. Ve a la sección **"Explotación de datos"**
3. Selecciona **"Evaluación"**
4. Selecciona **"Alumnos con materia y notas"**
5. Haz clic en **"CSV"** para descargar el archivo
6. Guarda el archivo en tu ordenador

El archivo descargado tendrá un nombre similar a:
```
DescargaExpGesExpDat_YYYYMMDD_HHMMSS_XXXXXX.CSV
```

### Paso 2: Analizar los datos

#### Opción A: Uso en línea (Recomendado)

1. Ve a la aplicación web: [https://elenafp.github.io/raices-analisis-notas/](https://elenafp.github.io/raices-analisis-notas/)
2. Carga el archivo CSV:
   - **Opción 1**: Haz clic en "Seleccionar archivo CSV"
   - **Opción 2**: Arrastra y suelta el archivo sobre el área de carga
3. Los resultados se mostrarán automáticamente organizados por pestañas (1ª Ev, 2ª Ev, etc.).

#### Opción B: Uso local (Offline)

1. Descarga el archivo `index.html` de este repositorio
2. Haz doble clic en el archivo para abrirlo en tu navegador
3. Sigue los mismos pasos que en la Opción A

## 🛠️ Funcionalidades Avanzadas

### Agrupación de Unidades
Si quieres ver las estadísticas consolidadas por nivel (ej. todo 1º de ESO junto) en lugar de por clase individual:

1. Haz clic en el botón **"⚙️ Reconfigurar Grupos"** (o aparecerá automáticamente al cargar).
2. Selecciona las clases que quieras unir (ej. 1º ESO A, 1º ESO B).
3. Escribe un nombre para el grupo (ej. "1º ESO") en la casilla superior.
4. Haz clic en **"Agrupar Seleccionados"**.
5. Cuando termines, pulsa **"Ver Resultados ➡️"**.

### Descarga de Resultados
En cada pestaña de evaluación (1ª, 2ª, Final...), encontrarás un botón **"⬇️ Descargar CSV"**. Esto generará un archivo Excel/CSV con la tabla de resultados que estás viendo en pantalla para que puedas guardarla o trabajar con ella.

## 📋 Información mostrada

Para cada grupo, la herramienta calcula:

| Columna | Descripción |
|---------|-------------|
| **GRUPO** | Nombre del grupo o unidad |
| **ALUMNOS** | Número total de alumnos matriculados |
| **TODO APROBADO** | Alumnos con 0 suspensos |
| **1 SUSPENSO** | Alumnos con exactamente 1 asignatura suspensa |
| **2 SUSPENSOS** | Alumnos con exactamente 2 asignaturas suspensas |
| **3 SUSPENSOS** | Alumnos con exactamente 3 asignaturas suspensas |
| **4+ SUSPENSOS** | Alumnos con 4 o más asignaturas suspensas |

### Lógica de cálculo
- **Nota < 5**: Se considera suspenso.
- **Normalización**: Soporta notas numéricas con decimales (coma o punto) y sufijos especiales como "-M" (Matrícula de Honor).
- **Evaluación Final**: Prioriza la columna `NOTAORD` y usa `EVFINAL(LOMLOE)` como respaldo si la primera está vacía.

## 🚀 Despliegue en GitHub Pages

Este repositorio está configurado para desplegarse automáticamente.

### Configuración (solo necesitas hacerlo una vez)

1. **Sube el repositorio a GitHub**
2. **Configura GitHub Pages**:
   - Ve a Settings → Pages
   - En "Source", selecciona: **GitHub Actions**
3. **¡Listo!** Cada vez que hagas push a `main`, se desplegará automáticamente.

Tu aplicación estará disponible en:
```
https://elenafp.github.io/raices-analisis-notas/
```

## 📄 Licencia

Este proyecto es de código abierto y está disponible para uso libre en centros educativos.