# DianaTesis
# Herramientas de Análisis de Bioseñales (EEG & EMG) en Python 🧠💪

Este repositorio contiene una colección de **Jupyter Notebooks** diseñados como material de consulta y aprendizaje para el **Procesamiento Digital de Señales (DSP)** aplicado a la Física Biomédica.

El proyecto guía al usuario a través de un flujo de trabajo completo ("pipeline"), desde la carga de datos crudos hasta el análisis espectro-temporal avanzado, utilizando librerías de código abierto en Python.

## 🎯 Objetivo
Proporcionar herramientas prácticas y reproducibles para analizar y comparar dos de las bioseñales más importantes:
* **Electroencefalografía (EEG):** Actividad oscilatoria de la corteza cerebral (Enfoque en ritmos y sincronización).
* **Electromiografía (EMG):** Actividad eléctrica de la contracción muscular (Enfoque en magnitud y fuerza).

## 📂 Contenido del Repositorio

El curso está dividido en 7 notebooks progresivos:

### 1. Fundamentos y Visualización
* **Notebook 1 (N1):** Introducción a la manipulación de series de tiempo biomédicas. Carga de archivos (CSV para EEG, WAV para EMG), manejo de estructuras de datos con `Pandas` y `NumPy`, y visualización inicial en el dominio del tiempo.

### 2. Pre-procesamiento Digital
* **Notebook 2 (N2):** Limpieza de la señal. Implementación de filtros digitales IIR (Butterworth) para eliminar *offsets* de DC, ruido de línea (60 Hz) y artefactos de movimiento. Uso de `filtfilt` para filtrado de fase cero.

### 3. Análisis Espectral Estacionario (EEG)
* **Notebook 3 (N3):** Transición al dominio de la frecuencia. Fundamentos de la FFT y estimación robusta de la **Densidad Espectral de Potencia (PSD)** mediante el **Método de Welch**. Cuantificación del fenómeno de **Bloqueo Alfa** (ojos abiertos vs. cerrados).

### 4. Análisis Tiempo-Frecuencia (STFT)
* **Notebook 4 (N4):** Análisis de señales no estacionarias. Introducción a la **Transformada de Fourier de Tiempo Corto (STFT)** y construcción de **espectrogramas** para visualizar la evolución temporal de la energía y la reactividad cerebral.

### 5. Análisis Adaptativo (Wavelet & Hilbert)
* **Notebook 5 (N5):** Técnicas avanzadas para superar el compromiso de resolución. Uso de la **Transformada Wavelet Continua (CWT)** para análisis multiescala y **Transformada de Hilbert** para la extracción de amplitud y frecuencia instantánea (dinámica del ritmo alfa).

### 6. Procesamiento Específico de EMG vs. EEG
* **Notebook 6 (N6):** Comparativa metodológica. Implementación del protocolo estándar para EMG: **Rectificación y Envolvente** (vía Hilbert). Discusión sobre por qué el procesamiento de EEG (oscilatorio) difiere del EMG (magnitud de activación).

### 7. Análisis Espectral Comparativo
* **Notebook 7 (N7):** Caracterización espectral del músculo. Análisis de la distribución de energía de banda ancha del EMG, cálculo de la **Frecuencia Mediana** como indicador de fatiga y contraste final con la estructura rítmica del EEG.

---

## 🛠️ Requisitos e Instalación

Este proyecto utiliza **Python 3.x**. Las principales dependencias son:

* `numpy`
* `scipy`
* `matplotlib`
* `pandas`
* `pycwt` (Para análisis Wavelet)
* `spkit` (Herramientas avanzadas de señal)

Para instalar las dependencias necesarias, puedes ejecutar el siguiente comando:

```bash
pip install numpy scipy matplotlib pandas pycwt spkit
## 📊 Datos Utilizados

Los notebooks utilizan datos reales provenientes de protocolos experimentales académicos:

1.  **EEG:** Registros de **Emotiv EPOC+** (14 canales, 128 Hz). Protocolo de reposo visual (Ojos Abiertos / Ojos Cerrados).
    * *Fuente:* Práctica de Saldaña Enciso & González González (Facultad de Ciencias, UNAM).
2.  **EMG:** Registros de **Backyard Brains SpikerBox** (1 canal, 44.1 kHz). Contracciones intermitentes del músculo gastrocnemio.
    * *Fuente:* Repositorio *Electrophysiology Basics* (McKiernan, 2025).

## 📖 Referencias y Créditos

Este trabajo fue desarrollado como parte del reporte de práctica profesional para la titulación de **Físico Biomédico** en la **Facultad de Ciencias, UNAM**.

**Autor:** Diana Zoila Vázquez Pérez.

**Agradecimientos especiales:**
* A la **Dra. Erin McKiernan** por su mentoría, materiales de enseñanza abierta y el código base para el análisis de EMG.
* Al proyecto *Electrophysiology Basics* por promover la ciencia abierta y la reproducibilidad.

## 📄 Licencia

Este proyecto se distribuye bajo la licencia [MIT](LICENSE), fomentando el uso libre, la modificación y la distribución con la debida atribución.