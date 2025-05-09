# TDA-futbol-11ideal

## 📄 Descripción

Este repositorio contiene el desarrollo del proyecto **"Formación de un equipo ideal de fútbol utilizando Análisis Topológico de Datos (TDA)"**. Se utiliza KeplerMapper para construir un grafo topológico sobre jugadores reales, analizando sus características físicas, técnicas y mentales. A partir de este grafo, se identifican regiones representativas por posición (porteros, defensas, medios, delanteros) y se selecciona un equipo balanceado y funcional de 11 jugadores.

## 📁 Estructura del repositorio

```bash
.
├── data/                        # Datos originales
│   └── players_22.csv           # Base de datos de jugadores
├── notebooks/                   # Notebook principal del análisis
│   └── EquipoIdeal_TDA.ipynb
├── requirements.txt             # Paquetes necesarios
└── README.md                    # Este archivo
```

## 🚀 Uso

1. Abre el notebook en Jupyter o Google Colab:

   ```bash
   jupyter lab notebooks/EquipoIdeal_TDA.ipynb
   ```

2. Ejecuta el notebook siguiendo las secciones: limpieza, análisis topológico, construcción del grafo y selección del equipo.

## 🧭 Estructura del Notebook

1. **Planteamiento del Problema**  
   Se busca construir un 11 titular ideal utilizando TDA para capturar la estructura del rendimiento de los jugadores y formar un equipo equilibrado por posiciones y estilo de juego.

2. **Metodología**

   * Carga y limpieza de datos: se seleccionaron variables físicas, técnicas y mentales, excluyendo valor comercial.
   * Normalización con `StandardScaler`.
   * Filtro topológico: combinación de UMAP y densidad como filtro 2D para capturar tanto la estructura latente del rendimiento como las zonas de mayor concentración de jugadores.
   * Construcción del grafo con KeplerMapper: se segmenta el espacio proyectado, se agrupan jugadores con DBSCAN y se conectan nodos que comparten puntos para revelar la forma topológica del espacio de habilidades.
   * Análisis del grafo: se identificaron los nodos más relevantes a partir de su tamaño y conectividad, y se analizaron en función de los jugadores que contenían. A partir de los nombres presentes y sus perfiles conocidos, se seleccionaron nodos que representaban claramente distintas posiciones (porteros, defensas, mediocampistas y atacantes), lo que permitió construir un equipo balanceado con base en zonas bien definidas del grafo topológico.
   * Selección del 11: se extrajeron jugadores representativos de cada nodo (centrales o bien conectados) y se mostraron junto con su posición original.

3. **Resultados y análisis**

4. **Conclusiones**

5. **Referencias**

## 📸 Capturas de Pantalla
Grafo Mapper (zonas por posición)

<img width="329" alt="image" src="https://github.com/user-attachments/assets/3ccf19c7-70ba-4546-8ce1-ebb6a3b5a387" />


11 Ideal formado

<img width="295" alt="image" src="https://github.com/user-attachments/assets/3999a1bb-35d5-4e5c-900a-5c2605fa2db5" />


## 📈 Resultados Clave

* Visualización topológica de perfiles de jugadores.
* Identificación de agrupamientos claros por posición.
* Selección de jugadores representativos por nodo, formando un equipo equilibrado y justificado por la estructura del grafo.
* Demostración de que TDA permite construir soluciones funcionales y explicables más allá de los rankings tradicionales.
