# INSTALACIÓN QINTEGRITY

## Requisitos Previos

- **Windows 10 o superior**
- **Python 3.8 o superior** (descargar de https://www.python.org/downloads/)

## Pasos de Instalación

### 1. **Preparación (Primera vez)**

Si **NO tiene Python instalado** en su computador:
1. Descargue Python desde: https://www.python.org/downloads/
2. **IMPORTANTE**: Durante la instalación, marque la opción **"Add Python to PATH"**
3. Reinicie su computador después de instalar Python

### 2. **Ejecutar el Instalador**

1. Descomprima el archivo descargado en la carpeta donde desee instalar QIntegrity
2. Haga **doble clic** en `INSTALADOR.bat`
3. Siga las instrucciones que aparezcan en pantalla
4. El proceso instalará automáticamente:
   - Entorno virtual de Python
   - Todas las dependencias necesarias
   - Tesseract OCR (sistema de reconocimiento de texto)

### 3. **Instalación de Tesseract OCR**

Durante la instalación, es posible que se le solicite descargar Tesseract OCR:

1. Haga clic en el enlace proporcionado o visite:
   https://github.com/UB-Mannheim/tesseract/wiki

2. Descargue: **tesseract-ocr-w64-setup-v5.x.exe**

3. Ejecute el instalador y recuerde la ruta de instalación (por defecto: `C:\Program Files\Tesseract-OCR`)

4. Cuando se le pida en el instalador de QIntegrity, ingrese la ruta de Tesseract

### 4. **Ejecutar la Aplicación**

Después de la instalación, simplemente:
- **Haga doble clic en `EJECUTAR.bat`**

O abra una terminal en la carpeta del proyecto y ejecute:
```
EJECUTAR.bat
```

La aplicación se abrirá automáticamente en su navegador en: `http://localhost:8501`

## Solución de Problemas

### "Python no está instalado"
- Verifique que Python esté instalado: Abra Terminal y escriba `python --version`
- Si no funciona, instale Python desde https://www.python.org/downloads/
- **NO OLVIDE marcar "Add Python to PATH"** durante la instalación

### "No se encontró Tesseract"
- Es necesario instalar Tesseract OCR manualmente
- Descargue desde: https://github.com/UB-Mannheim/tesseract/wiki
- Ejecute el instalador y use la ruta indicada durante el setup

### "Error al instalar dependencias"
- Asegúrese de tener conexión a Internet
- Si el error persiste, ejecute manualmente en terminal:
  ```
  call venv\Scripts\activate.bat
  pip install -r requirements.txt
  ```

### "El puerto 8501 ya está en uso"
- Streamlit intentará usar el puerto 8502, 8503, etc. automáticamente
- O puede especificar un puerto diferente

## Desinstalación

Para desinstalar QIntegrity:
1. Ejecute `DESINSTALAR.bat`
2. O simplemente elimine toda la carpeta del proyecto

## Actualización de Dependencias

Si necesita actualizar las dependencias en el futuro:
1. Abra Terminal en la carpeta del proyecto
2. Ejecute:
   ```
   call venv\Scripts\activate.bat
   pip install --upgrade -r requirements.txt
   ```

## Estructura del Proyecto

```
QIntegrity/
├── INSTALADOR.bat          # Ejecutable para instalar
├── EJECUTAR.bat            # Ejecutable para ejecutar
├── DESINSTALAR.bat         # Ejecutable para desinstalar
├── app.py                  # Aplicación principal
├── api_ia.py               # API de IA
├── requirements.txt        # Dependencias de Python
├── venv/                   # Entorno virtual (creado tras instalar)
└── [otros archivos...]
```

## Soporte

Si experimenta problemas:
1. Verifique que todos los requisitos previos estén instalados
2. Intente ejecutar `INSTALADOR.bat` nuevamente
3. Elimine la carpeta `venv` y repita la instalación

---

**Versión**: 1.0  
**Fecha**: 2026-02-06
