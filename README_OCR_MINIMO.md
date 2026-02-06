# Instrucciones para: `demoV3` 

Pasos para probar la `app.py` y la función del motor OCR

1) Crear y activar entorno virtual (recomendado si no funciona con el .bat):
   python -m venv .venv
   .\.venv\Scripts\activate

2) Instalar dependencias del requirements.txt:
   python -m pip install --upgrade pip
   pip install PyMuPDF pdf2image pytesseract langdetect
   ocrmypdf: pip install ocrmypdf
   groq: pip install groq

3) Instalar binarios del sistema:
   - Tesseract OCR (debe disponer del idioma 'spa'). Verificar:
     tesseract --version
   - Poppler (contiene pdftoppm) para `pdf2image`. Verificar:
     pdftoppm -v
   Si los binarios no están en PATH, definir variables (PowerShell):
     setx POPPLER_PATH "C:\\ruta\\a\\poppler\\bin"
     setx TESSERACT_CMD "C:\\Program Files\\Tesseract-OCR\\tesseract.exe"
   (Cerrar y volver a abrir la terminal después de setx.)

4) Ejecutar la app:
   pip install streamlit
   streamlit run app.py

Notas:
- El resultado del OCR se guarda en `archivo.pdf.ocr.txt` (misma carpeta que el PDF) para evitar reprocesos.
- instala `qpdf` y `ghostscript` para optimizaciones .
