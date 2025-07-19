# 📄 SALVADOR_DE_SIMILITUD_2025

Repositorio del proyecto **SALVADOR_DE_SIMILITUD_2025**, una herramienta desarrollada en **Python 🐍** que permite insertar ceros invisibles (`"0"` con color blanco) en documentos de Word a partir de la segunda página, con el fin de alterar la similitud detectada por herramientas de análisis de plagio.

## 🧩 Descripción del Proyecto

Este programa escanea un archivo `.docx` de Microsoft Word y, a partir de la **página 2**, recorre los párrafos e inserta un `"0"` blanco cada cierta cantidad de caracteres (por defecto cada 70), sin alterar el contenido visible para el lector. La idea es romper la similitud textual sin cambiar la estructura visual del documento.

## 🧩 Tecnologías utilizadas

- ![Python](https://img.shields.io/badge/-Python-3776AB?logo=python&logoColor=white&style=flat-square) Python 3.x
- ![Tkinter](https://img.shields.io/badge/-Tkinter-yellow?style=flat-square&logo=python) Interfaz gráfica
- 🧩 `win32com.client` (automatización de Microsoft Word)
- 🧠 Lógica basada en inserción estratégica de ceros blancos invisibles en documentos `.docx`

## 🗂️ Estructura

```
SALVADOR_DE_SIMILITUD_2025/
│
├── salvador.py         # Código fuente principal
├── README.md           # Este archivo
```

## 💡 ¿Cómo funciona?

1. Seleccionas un archivo `.docx` usando la interfaz gráfica.
2. El script abre el documento con Word (en segundo plano).
3. A partir de la segunda página, agrega un "0" invisible cada cierta cantidad de caracteres.
4. Guarda una copia en una carpeta llamada `MODIFICADO/` con el sufijo `_modificado.docx`.
5. Abre automáticamente el documento modificado.

## ▶️ Ejecución

1. Asegúrate de tener Python y Microsoft Word instalados en tu PC con Windows.
2. Instala la librería necesaria si no la tienes:
   ```bash
   pip install pywin32
   ```
3. Ejecuta el script:

   ```bash
   python salvador.py
   ```

4. Se abrirá una ventana donde puedes seleccionar un archivo Word.

## 📝 Código Principal (resumen)

```python
import win32com.client as win32
import tkinter as tk
from tkinter import filedialog, messagebox

# Se abre el documento Word
# Se recorren los párrafos desde página 2
# Cada 70 caracteres se inserta un "0" invisible
# Se guarda el nuevo archivo en MODIFICADO/
```

## 📌 Observaciones

- El documento original **no se modifica**.
- Se recomienda usar solo en documentos finales, ya que los "0" ocultos pueden alterar búsquedas internas o copiar/pegar.
- La herramienta es experimental y de uso educativo.

## 📋 Licencia

Distribuido con fines educativos. Uso bajo responsabilidad del usuario.

---

Desarrollado por [Francisco Campos Sandi](https://github.com/Francisco-Campos-S) 🧠 con fines académicos.

