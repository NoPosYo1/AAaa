# Instrucciones para: `QIntegrity` 

Pasos para probar el proyecto

1) Instalar dependencias del requirements.txt:
   python -m pip install --upgrade pip
    ````
   pip install ^
    streamlit ^
    pandas ^
    numpy ^
    openpyxl ^
    matplotlib ^
    groq ^
    pdf2image ^
    python-docx ^
    pymupdf ^
    langdetect ^
    rapidocr-onnxruntime ^
    opencv-python-headless 
    ````

2) Ejecutar la app desde dentro de la carpeta del proyecto: 
   ````streamlit run app.py````

Notas:
- El resultado del OCR se guarda en `archivo.pdf.ocr.txt` (misma carpeta que el PDF) para evitar reprocesos.
