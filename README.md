# Company Valuation Web App

Esta es una aplicación web sencilla creada con [Streamlit](https://streamlit.io/) que permite descargar los datos financieros de una empresa desde Yahoo Finance (usando `yfinance`) y volcarlos automáticamente en la plantilla Excel de valoración IDC.

## ¿Cómo funciona?

La aplicación obtiene los datos del "Income Statement", "Balance Sheet" y "Cash Flow" del Ticker introducido, y los inyecta en las pestañas `7.TIKR_IS`, `8.TIKR_BS` y `9.TIKR_CF` de la plantilla Excel proporcionada. Luego te permite descargar el Excel relleno.

## Instalación y Uso

Sigue estos pasos para ejecutar la aplicación en tu propio ordenador:

1. Asegúrate de tener Python instalado en tu sistema.
2. Clona este repositorio o descarga los archivos.
3. Abre una terminal (o consola de comandos) en la carpeta del proyecto.
4. Instala las dependencias necesarias ejecutando el siguiente comando:
   ```bash
   pip install -r requirements.txt
   ```
5. Inicia la aplicación de Streamlit ejecutando:
   ```bash
   streamlit run app.py
   ```
6. Se abrirá automáticamente una pestaña en tu navegador web (normalmente en `http://localhost:8501`). Si no se abre, copia y pega ese enlace en tu navegador.
7. ¡Listo! Introduce el Ticker de la empresa (ej: AAPL, MSFT) y haz clic en "Generar Excel" para descargar tu plantilla.

> **Nota importante:** Dado que los nombres de las métricas que utiliza Yahoo Finance difieren de los que utiliza la plataforma TIKR, es posible que algunas fórmulas de las hojas de cálculo (1.IS, 2.FCF, 3.ROIC, etc.) que dependen de nombres exactos no se completen solas. Tendrás que ajustar las celdas marcadas en azul/naranja o remapear los nombres en las hojas de fórmulas.
