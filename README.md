# **Documentación del Proyecto**

## **Monitoreo de Seguridad de Red**

### **Descripción del Proyecto**

Este proyecto se centra en la implementación de un sistema de monitoreo de seguridad de red que utiliza técnicas de machine learning para detectar posibles intrusiones analizando el tráfico de red en tiempo real.

### **Estructura del Proyecto**

proyecto\_segu\_inf/

├── captura/

│   ├── analisis\_paquetes.py

│   ├── captura\_paquetes.py

│   ├── deteccion\_intrusiones.py

│   ├── entrenar\_modelo.py

│   └── \_\_pycache\_\_/

├── intrusions.db

├── logs/

│   └── intrusiones.log

├── modelos/

│   └── modelo.pkl

└── web/
    ├── app.py

    └── templates/

        └── statistics.html

### **Componentes Principales**

1. **Entrenamiento del Modelo de Machine Learning**  
   * Archivo: `captura/entrenar_modelo.py`  
2. **Captura y Análisis de Paquetes**  
   * Archivo: `captura/analisis_paquetes.py`  
   * Archivo: `captura/captura_paquetes.py`  
3. **Servidor Web para Visualización de Estadísticas**  
   * Archivo: `web/app.py`  
   * Archivo: `web/templates/statistics.html`

   ### **Base de Datos**

* Archivo: `intrusions.db`  
* Tabla `intrusions`:  
  * `id`: INTEGER PRIMARY KEY AUTOINCREMENT  
  * `ip`: TEXT NOT NULL  
  * `timestamp`: DATETIME DEFAULT CURRENT\_TIMESTAMP

  ### **Ejecución del Proyecto**

  **Activar el Entorno Virtual:**  
    bash  
    python3 \-m venv env

  source env/bin/activate

1.   
   **Entrenar el Modelo:**  
   bash  
   python3 captura/entrenar\_modelo.py  
2.   
   **Capturar y Analizar Paquetes:**  
   bash  
   python3 captura/captura\_paquetes.py  
3.   
   **Iniciar el Servidor Flask:**  
   bash  
   python3 web/app.py  


   ### **Notas Finales**

Este proyecto utiliza técnicas de machine learning para detectar patrones de tráfico anómalos y posibles intrusiones en una red. La integración con una base de datos SQLite permite registrar y analizar las intrusiones detectadas, y la interfaz web facilita la visualización de estas estadísticas.

