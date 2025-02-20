##Documentación del Proyecto

##Monitoreo de Seguridad de Red

Descripción del Proyecto
Este proyecto se centra en la implementación de un sistema de monitoreo de seguridad de red que utiliza técnicas de machine learning para detectar posibles intrusiones analizando el tráfico de red en tiempo real.

Estructura del Proyecto

proyecto_segu_inf/

├── captura/

│   ├── analisis_paquetes.py

│   ├── captura_paquetes.py

│   ├── deteccion_intrusiones.py

│   ├── entrenar_modelo.py

│   └── __pycache__/

├── intrusions.db

├── logs/

│   └── intrusiones.log

├── modelos/

│   └── modelo.pkl

└── web/

    ├── app.py
    
    └── templates/
    
        └── statistics.html
        
Componentes Principales

Entrenamiento del Modelo de Machine Learning

Archivo: captura/entrenar_modelo.py

Captura y Análisis de Paquetes

Archivo: captura/analisis_paquetes.py

Archivo: captura/captura_paquetes.py

Servidor Web para Visualización de Estadísticas

Archivo: web/app.py

Archivo: web/templates/statistics.html

Base de Datos

Archivo: intrusions.db

Tabla intrusions:

id: INTEGER PRIMARY KEY AUTOINCREMENT

ip: TEXT NOT NULL

timestamp: DATETIME DEFAULT CURRENT_TIMESTAMP

Ejecución del Proyecto

Activar el Entorno Virtual:

bash

python3 -m venv env
source env/bin/activate


Entrenar el Modelo:

bash

python3 captura/entrenar_modelo.py
Capturar y Analizar Paquetes:

bash

python3 captura/captura_paquetes.py
Iniciar el Servidor Flask:

bash
python3 web/app.py

Notas Finales
Este proyecto utiliza técnicas de machine learning para detectar patrones de tráfico anómalos y posibles intrusiones en una red. La integración con una base de datos SQLite permite registrar y analizar las intrusiones detectadas, y la interfaz web facilita la visualización de estas estadísticas.
