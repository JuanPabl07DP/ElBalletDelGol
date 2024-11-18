# 🏆 El Ballet del Gol.
## Inspirado en EA Sports FC 25

## Creado por: Juan Pablo Daza Pereira y Juan Sebastian Camargo Sanchez

Este proyecto implementa un algoritmo basado en **colonia de hormigas (ACO)** para determinar el **mejor camino hacia el gol** en un equipo de fútbol. Utilizando estadísticas de los jugadores y simulando decisiones de pase, este modelo identifica las rutas más óptimas para maximizar la probabilidad de anotación.

---

## ⚙️ Funcionalidades

- **Probabilidad de gol**: Calcula la probabilidad de anotar en base a atributos del jugador (disparo, control y visión).
- **Peso del pase**: Evalúa la dificultad de los pases, tomando en cuenta si son cortos o largos y considerando las habilidades del jugador.
- **Algoritmo de colonia de hormigas (ACO)**: Simula la toma de decisiones para encontrar la ruta de ataque con la mayor probabilidad de éxito.
- **Visualización**: Grafica el equipo en el campo, mostrando las rutas con probabilidades de pase y tiro a gol, resaltando la mejor ruta encontrada.

---

## 📊 Estructura del Proyecto

- **Posiciones de Jugadores** (`PLAYER_POSITIONS`): Mapa de posiciones y nombres en el equipo.
- **Probabilidades y Pesos**:
  - `calculate_goal_probability`: Calcula la probabilidad de gol de un jugador en base a sus estadísticas.
  - `calculate_pass_weight`: Determina la dificultad de pases cortos o largos entre jugadores.
- **Algoritmo ACO**:
  - **Colonia de Hormigas**: Simula rutas con agentes ("hormigas") usando probabilidad basada en feromonas y pesos de pase.
  - **Actualización de Feromonas**: Refuerza las rutas exitosas y evapora aquellas sin resultado óptimo.
- **Generación y Visualización del Grafo**: Representa las posiciones y probabilidades en un campo 4-3-3 y muestra la mejor ruta de ataque.

---

## 🚀 Cómo Usarlo

1. **Instalar Dependencias**: Asegúrate de tener `networkx` y `matplotlib` instalados.
    ```bash
    pip install networkx matplotlib
    ```

2. **Ejecutar el Script**:
    ```bash
    python script.py
    ```
   Esto generará un grafo visual con el camino óptimo resaltado en rojo.

3. **Parámetros Clave**:
   - `agents`: Número de agentes en el algoritmo ACO.
   - `iterations`: Número de iteraciones del algoritmo.
   - `tau` y `ro`: Parámetros de ajuste de feromonas para explorar/explotar rutas.

---

## 📈 Ejemplo de Visualización

La visualización muestra el equipo en una **formación 4-3-3**, con:
- Rutas grises (pases generales) y en rojo (mejor camino de ataque).
- Peso de los pases y probabilidades de gol en cada segmento de la ruta.

---

## 🛠 Futuras Mejoras

- **Adaptabilidad de Formaciones**: Expansión a diferentes formaciones (4-4-2, 3-5-2, etc.).
- **Parámetros de Juego Dinámicos**: Ajuste dinámico de probabilidades y pesos basado en contexto del juego.
- **Análisis Estadístico Avanzado**: Incorporación de datos avanzados para mejor precisión en las decisiones de pase y tiro.
