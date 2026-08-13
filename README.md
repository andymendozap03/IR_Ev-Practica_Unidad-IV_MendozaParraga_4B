# Prueba Práctica — Unidad IV · Paralelo B
### Ingeniería de Requisitos (ISR-401) — UTEQ

**Caso práctico:** Sistema de Reserva de Citas Médicas
**Estudiante:** Mendoza Párraga Andy Johel — CI: 1251401590 — amendozap9@uteq.edu.ec
**Curso/Paralelo:** Cuarto semestre, Paralelo "B"
**Docente:** Ing. Gleiston Guerrero, Mg.
**Modalidad:** Individual, en clase
**Fecha:** 12/08/2026

**Repositorio:** https://github.com/andymendozap03/IR_Ev-Practica_Unidad-IV_MendozaParraga_4B.git

---

## 1. Compilación

### Compilador
`pdflatex` (TeX Live / MiKTeX). El documento usa el sistema de bibliografía clásico **BibTeX** (`natbib` + `plainnat`) — **no usar biber**, ya que el proyecto no está configurado con `biblatex` y biber no procesará las citas.

### Orden de comandos

Desde la raíz del repositorio, ejecutar en este orden exacto:

```bash
pdflatex MendozaParraga_Evaluacion_U4.tex
bibtex MendozaParraga_Evaluacion_U4
pdflatex MendozaParraga_Evaluacion_U4.tex
pdflatex MendozaParraga_Evaluacion_U4.tex
```

Se requieren las dos pasadas finales de `pdflatex` para resolver correctamente las referencias cruzadas, el índice de figuras y las citas bibliográficas (`\citep{}`) generadas por `bibtex`.

**En Overleaf:** en el menú de configuración del proyecto (ícono ☰ → *Settings*), verificar que **"Bibliography engine"** esté establecido en **`Bibtex`** (no `Biber`), y que el **compilador** sea `pdfLaTeX`.

### Archivo principal
`MendozaParraga_Evaluacion_U4.tex`

### Dependencias

**Paquetes LaTeX** (todos incluidos en una distribución TeX Live/MiKTeX completa, sin paquetes adicionales que instalar):

`inputenc`, `fontenc`, `helvet`, `textcomp`, `geometry`, `amsmath`, `amssymb`, `graphicx`, `xcolor` (opciones `table`, `dvipsnames`), `array`, `tabularx`, `multirow`, `colortbl`, `booktabs`, `enumitem`, `microtype`, `parskip`, `titlesec`, `fancyhdr`, `caption`, `pdflscape`, `natbib` (opciones `numbers`, `sort&compress`), `hyperref`, `tcolorbox` (opciones `skins`, `breakable`), `float`.

**Archivos de datos:**
- `referencias.bib` — base bibliográfica (6 entradas: Fagan 1976, ISO/IEC 25010:2023, ISO/IEC/IEEE 29148:2018, OMG UML 2.5.1, Pohl 2010, SWEBOK Guide v4.0).

**Imágenes** (carpeta `figuras/`, formato PNG, referenciadas por `\includegraphics`):
- `Diagrama_Clases_Citas.png` — P1, diagrama de clases UML.
- `Diagrama_Actividades_Citas.png` — P2, diagrama de actividades UML (v1.0).
- `Diagrama_MaquinasEstado_Citas.png` — P3, máquina de estados UML.
- `Diagrama_ActividadesCorregido_Citas.png` — P4, diagrama de actividades corregido (v1.1).
- `Resumen_Evaluacion_LMS.png` — evidencia SGA, resumen del cuestionario.
- `Revision_intento_lms.png` — evidencia SGA, revisión del intento.
- `revision_pg-1.png` … `revision_pg-8.png` — anexo con la revisión de intento completa (8 páginas), incrustadas a página completa sin encabezado ni pie.

No se requiere ningún paquete `.sty` externo ni descarga adicional: todos los paquetes listados forman parte de una instalación estándar de TeX Live (`texlive-full`) o MiKTeX con instalación automática de paquetes activada.

---

## 2. Estructura del repositorio

```
IR_Ev-Practica_Unidad-IV_MendozaParraga_4B/
├── MendozaParraga_Evaluacion_U4.tex   # Archivo principal (fuente LaTeX)
├── referencias.bib                    # Base bibliográfica (BibTeX)
├── README.md                          # Este archivo
├── MendozaParraga_Evaluacion_U4.pdf   # PDF compilado (entregable final)
└── figuras/
    ├── Diagrama_Clases_Citas.png
    ├── Diagrama_Actividades_Citas.png
    ├── Diagrama_MaquinasEstado_Citas.png
    ├── Diagrama_ActividadesCorregido_Citas.png
    ├── Resumen_Evaluacion_LMS.png
    ├── Revision_intento_lms.png
    ├── revision_pg-1.png
    ├── revision_pg-2.png
    ├── revision_pg-3.png
    ├── revision_pg-4.png
    ├── revision_pg-5.png
    ├── revision_pg-6.png
    ├── revision_pg-7.png
    └── revision_pg-8.png
```

---

## 3. Contenido del documento

El PDF compilado contiene, en este orden:

1. **Carátula** con datos de identificación, URL del repositorio (en una sola línea) y evidencia del cuestionario rendido en el SGA (capturas de resumen y de revisión del intento).
2. **Instrucciones generales y entregables**, **criterios de piso** y **caso práctico** (Sistema de Reserva de Citas Médicas), transcritos del instrumento de evaluación.
3. **Actividades prácticas P1–P10** (70 puntos): diagrama de clases, diagrama de actividades, máquina de estados, tabla de consistencia entre perspectivas (con corrección aplicada), especificación de requisitos con esquema de atributos, priorización MoSCoW, inspección 29148, pruebas de aceptación trazadas, matriz de trazabilidad y gestión del cambio con línea base.
4. **Rúbrica de evaluación** (componente SGA 30 % + componente práctico 70 %).
5. **Marco normativo de referencia** con las 6 citas bibliográficas y su listado final.
6. **Anexo:** revisión de intento completa del cuestionario del SGA (8 páginas, incrustadas a página completa).

---


## 4. Notas para la reproducción

- Clonar el repositorio completo (incluida la carpeta `figuras/` y el archivo `referencias.bib`) antes de compilar; el documento no compilará correctamente si falta alguno de estos archivos.
- No es necesario instalar ningún paquete adicional fuera de una distribución LaTeX estándar.
- Si se compila en un editor online (Overleaf) o local con soporte de perfiles de compilación, seleccionar explícitamente el motor **BibTeX**, no Biber.
