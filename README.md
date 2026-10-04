# Evaluador Bioinstrumental Kinésico de Sentadilla

Sistema de análisis kinemático en tiempo real para la evaluación del valgo y varo dinámico de rodilla durante la ejecución de la sentadilla (*squat*), mediante bioinstrumentación basada en visión por computadora e inteligencia artificial.

## 🔗 Enlaces del Proyecto
* **Interfaz Web Pública (Netlify):** https://analisisentadilla.netlify.app/
* **Repositorio de Código (GitHub):** https://github.com/tomaslopezl-cell/Evaluadorsentadilla
---

## 📋 Requisitos del Sistema
* **Navegador Web:** Compatibilidad nativa con Google Chrome, Microsoft Edge, Mozilla Firefox o Safari (con soporte para WebGL y HTML5 Canvas).
* **Dispositivo de Captura:** Cámara web integrada o USB (resolución mínima recomendada: 640x480 px).
* **Permisos:** Acceso autorizado a la cámara web en el navegador.

---

## 📦 Dependencias y Librerías
El proyecto no requiere instalación de paquetes locales via `npm` ni compilación de servidor, ya que consume los modelos y motores directamente desde CDN:

1. **TensorFlow.js Core (`@tensorflow/tfjs-core` v4.x):** Motor de procesamiento y ejecución de modelos de IA en el cliente.
2. **TensorFlow.js Backend WebGL (`@tensorflow/tfjs-backend-webgl`):** Aceleración por GPU para inferencia en tiempo real.
3. **MoveNet Pose Detection (`@tensorflow-models/pose-detection`):** Modelo *Thunder Single-Pose* optimizado para la detección de 17 puntos articulares (*keypoints*).

---

## 🚀 Instrucciones de Ejecución

### Opción 1: Enlace Público (Recomendado)
1. Acceder al enlace directo de Netlify proporcionado arriba.
2. Conceder permisos de uso de la cámara web al navegador.
3. Hacer clic en el botón **"Iniciar Cámara Web"**.
4. Posicionarse frente a la cámara a una distancia que permita encuadrar las extremidades inferiores en su totalidad.

### Opción 2: Ejecución Local
1. Descargar o clonar este repositorio en tu equipo.
2. Abrir directamente el archivo `index.html` en tu navegador preferido.
3. Hacer clic en **"Iniciar Cámara Web"** y permitir el acceso a la cámara.

---

## 📁 Archivos Principales
* **`index.html`:** Archivo monolítico que integra:
  * **Estructura HTML5:** Paneles de métricas, layout *side-by-side* para video e interfaz gráfica.
  * **Estilos CSS3:** Interfaz oscura (*dark mode*) responsiva optimizada para biofeedback visual.
  * **Lógica JavaScript:** 
    * Captura de video en tiempo real.
    * Estimación de puntos articulares (cadera, rodilla, tobillo).
    * Cálculo trigonométrico de ángulos cinemáticos.
    * Clasificación clínica por rangos fisiológicos (verde, amarillo, rojo).
    * Detección de fases del movimiento y tiempo mantenido en riesgo.
    * Renderizado continuo de gráficos sobre HTML5 Canvas.
* **`README.md`:** Documentación técnica del proyecto.
