![Logo](https://raw.githubusercontent.com/AdrianCastroC/DXPPTarea2/main/Logo_DishDash.png)
# Game Design Document – DISH DASH Restaurante Cooperativo

---

# 1. Game Concept (UD02)

## 1.1 Temática

Gestión de un restaurante caótico donde varios cocineros cooperan para atender oleadas crecientes de clientes. El foco está en la **organización**, la **cooperación** y la **optimización progresiva del espacio de trabajo**.

A medida que el restaurante crece, los jugadores deben reorganizar el entorno, mejorar las estaciones de trabajo y coordinarse para mantener la eficiencia del servicio.

El diseño del juego se centra en la coordinación entre jugadores y en la optimización del espacio del restaurante para mantener el ritmo del servicio.

### Pilares derivados de la temática

- Caos controlado  
- Cooperación local/online  
- Progresión entre días  
- Mejora progresiva mediante objetos upgradeables  

---

## 1.2 Género

- **Género principal:** Gestión / Simulación  
- **Subgéneros:** Party game cooperativo, Time management  

---

## 1.3 Público objetivo

El juego está orientado a jugadores que disfrutan de experiencias cooperativas rápidas y accesibles, especialmente fans de juegos como Overcooked o PlateUp!.

El diseño busca ser fácil de entender pero difícil de dominar, fomentando la coordinación entre jugadores y la optimización progresiva del restaurante.

---

## 1.4 Tipo de juego

Juego cooperativo de gestión por jornadas donde los jugadores preparan platos y atienden clientes dentro de un tiempo limitado.

Cada jornada funciona como un nivel independiente con dificultad progresiva. Si el restaurante fracasa durante el día, la jornada se reinicia, pero las mejoras y progreso del restaurante se mantienen.

Este sistema permite que los jugadores experimenten con diferentes estrategias de organización sin perder el progreso global del restaurante.

### Key Features

- Hasta 4 jugadores cooperativos
- Días progresivos con dificultad creciente
- Reinicio del día al perder sin perder progreso global
- Objetos de cocina mejorables que optimizan la eficiencia

---

## 1.5 Punto de vista

- **3D con cámara cenital / isométrica fija compartida**

Esta cámara permite visualizar el restaurante completo y facilita la coordinación entre jugadores.

---

## 1.6 Elevator Pitch

> Un restaurante cooperativo donde el caos se reinicia cada día, pero tu progreso no.

---

# 2. Mockup

**Mockup elegido:** HUD principal durante la partida.

El mockup representa la interfaz visible durante el gameplay, priorizando una lectura clara sin invadir el área de juego.

## Elementos del HUD

- Indicador de día y temporizador en la esquina superior izquierda  
- Contador de dinero visible en todo momento  
- Barra global de satisfacción de clientes en la parte superior  
- Órdenes de clientes mediante bocadillos con iconos de platos  
- Barra individual de paciencia para cada cliente  

El área central queda libre para el mapa y la acción.

![Mockup del HUD durante el gameplay](https://raw.githubusercontent.com/AdrianCastroC/DXPPTarea2/main/mockup_hud.png)

---

# 3. Método MoSCoW

## Must Have

- Juego cooperativo hasta 4 jugadores
- Sistema de días como niveles
- Preparación y servicio de platos
- Clientes con sistema de paciencia

## Should Have

- Progresión persistente
- Sistema de mejoras de estaciones de cocina

## Could Have

- Varias recetas
- Modificadores aleatorios de día

## Won’t Have (para esta versión)

- Matchmaking automático
- Chat de voz integrado
- Personalización estética avanzada

---

# 4. Inspiración

## Overcooked

- Interfaz clara
- Lectura rápida de información
- Caos cooperativo divertido

## PlateUp!

- Progresión estratégica
- Optimización del layout del restaurante
- Automatización progresiva

---

# 5. Mecánicas (UD03)

## 5.1 Core Loop

El bucle principal del juego se basa en la alternancia entre planificación y ejecución.

Fase de preparación → Inicio del servicio → Gestión de pedidos → Final del día → Mejora del restaurante → Nuevo día

Durante la fase de preparación los jugadores reorganizan el restaurante colocando estaciones, mesas y equipamiento con el objetivo de optimizar el flujo de trabajo.

Una vez comienza el servicio los clientes empiezan a llegar progresivamente y los jugadores deben coordinarse para preparar y entregar los pedidos antes de que los clientes pierdan la paciencia.

Al finalizar la jornada los jugadores reciben ingresos en función del rendimiento obtenido y pueden invertirlos en mejorar el restaurante para afrontar jornadas posteriores con mayor eficiencia.

### Objetivo del jugador

El objetivo principal de los jugadores es mantener el funcionamiento del restaurante durante cada jornada mientras optimizan progresivamente el espacio, las estaciones y la coordinación del equipo para afrontar niveles de dificultad cada vez mayores.

---

## 5.2 Tabla de Mecánicas

| Mecánica | Tipo | Descripción |
|--------|--------|--------|
| Movimiento del personaje | Primaria | Desplazamiento libre dentro del restaurante |
| Interacción con estaciones | Primaria | Uso de estaciones para cocinar o preparar ingredientes |
| Preparación de platos | Primaria | Secuencia de acciones necesarias para completar pedidos |
| Sistema de espera de clientes | Primaria | Cada cliente tiene un tiempo límite para recibir su pedido |
| Entrega de pedidos | Primaria | Entregar el plato correcto antes de que el cliente se marche |
| Fase de preparación | Secundaria | Tiempo previo al servicio donde se reorganiza el restaurante |
| Colocación de objetos | Secundaria | Sistema para posicionar mesas, cocinas y estaciones |
| Sistema de mejoras | Secundaria | Mejoras que optimizan velocidad o eficiencia |
| Reinicio del día | Secundaria | Permite repetir un día sin perder progreso global |
| Modificadores de día | Terciaria | Cambios en condiciones del servicio |
| Variedad de recetas | Terciaria | Introducción progresiva de nuevos platos |

---

## 5.3 Mecánicas del sistema / NPC

Además de las acciones directas del jugador, el juego incluye varios sistemas que afectan al comportamiento del restaurante y a la dinámica de la partida.

### Sistema de generación de clientes

Los clientes llegan al restaurante de forma progresiva durante la jornada.  
El ritmo de llegada aumenta a medida que avanzan los días, incrementando la presión sobre los jugadores.

### Sistema de paciencia de clientes

Cada cliente dispone de una barra de paciencia que disminuye con el tiempo.  
Si la paciencia se agota antes de recibir el pedido, el cliente abandona el restaurante.

Esto penaliza la barra global de satisfacción y reduce los ingresos obtenidos durante el día.

### Barra global de satisfacción

Representa la reputación general del restaurante durante la jornada.

La satisfacción disminuye cuando:
- Los clientes esperan demasiado
- Los pedidos se entregan incorrectamente
- Los clientes abandonan el restaurante

Si la satisfacción global cae demasiado el día puede terminar en fracaso.

### Escalado progresivo de dificultad

La dificultad del juego aumenta gradualmente mediante:

- Mayor número de clientes
- Recetas con más pasos de preparación
- Menor margen de error en la gestión del tiempo

---

## 5.4 Reglas del sistema

El funcionamiento del restaurante se rige por las siguientes reglas principales:

- Los clientes llegan de forma progresiva durante la jornada.
- Cada cliente dispone de un tiempo de espera limitado.
- Si un cliente abandona el restaurante se reduce la satisfacción global.
- Si la satisfacción global cae demasiado la jornada puede terminar en fracaso.
- Los pedidos deben entregarse correctamente para generar ingresos.
- Al final de cada jornada los jugadores reciben dinero en función del rendimiento.
- El dinero obtenido permite comprar o mejorar equipamiento del restaurante.
- Si una jornada fracasa se puede repetir sin perder el progreso global del restaurante.

---

# 6. Narrativa

## 6.1 Idea

Construir y optimizar un restaurante caótico hasta convertirlo en un negocio exitoso mediante cooperación y estrategia.

---

## 6.2 Logline

Un grupo de cocineros transforma un restaurante modesto en un negocio exitoso superando jornadas cada vez más caóticas donde el progreso permanece aunque el día se reinicie.

---

## 6.3 Sinopsis

El restaurante comienza como un pequeño negocio con recursos limitados.  
Los primeros días sirven para aprender a gestionar el espacio de trabajo y atender a los primeros clientes.

A medida que el restaurante gana popularidad, la afluencia de clientes aumenta y los pedidos se vuelven más complejos.  
Los jugadores deben reorganizar el restaurante, mejorar el equipamiento y optimizar el flujo de trabajo para mantener el servicio.

Aunque una jornada pueda fracasar, la experiencia obtenida y las mejoras adquiridas permiten que el restaurante evolucione progresivamente.

El objetivo final es transformar un restaurante caótico en un sistema perfectamente optimizado capaz de gestionar grandes cantidades de clientes de forma eficiente.

---

## 6.4 Arquetipo narrativo

El juego encaja en el arquetipo de **superación y progreso**.

### Desarrollo del arquetipo

1. Inicio: restaurante pequeño  
2. Conflicto: presión creciente del servicio  
3. Crisis: jornadas caóticas  
4. Adaptación: mejora del restaurante  
5. Resolución: restaurante optimizado  

---

## 6.5 Estructura narrativa

Acto I – Inicio del restaurante  
Acto II – Expansión y crecimiento  
Acto III – Dominio del sistema  
Inicio → Crecimiento → Crisis → Optimización → Éxito

---

## 6.6 Elementos narrativos adicionales

- Comentarios dinámicos de clientes  
- Eventos especiales entre jornadas  
- Noticias ficticias sobre el restaurante  
- Descripciones narrativas de mejoras  

---

# 7. Personajes

## Protagonista

### Nombre

El personaje no tiene un nombre fijo.  
Cada jugador registra su propio nombre, apodo o nickname al comenzar la partida.

Esto permite que el jugador se identifique directamente con su personaje y refuerza el carácter cooperativo del juego.

### Importancia

El protagonista representa al jugador dentro del restaurante.  
Cada jugador controla a uno de los cocineros encargados de gestionar el restaurante y atender a los clientes.

### Esfera física

- Cocinero del restaurante.
- Personaje genérico diseñado para representar a cualquier jugador.
- Su apariencia puede ser simple para mantener la claridad visual durante el gameplay.

### Esfera psicológica

- Cooperativo
- Resolutivo
- Capaz de adaptarse al caos del restaurante
- Enfocado en la eficiencia y la organización

### Transformación

La evolución del personaje no es narrativa sino **sistémica y estratégica**.

Al principio de la partida el jugador reacciona al caos del restaurante y a las tareas que aparecen.  
Con el progreso del juego el jugador aprende a anticipar problemas, optimizar el espacio de trabajo y coordinarse con otros jugadores.

La transformación consiste en pasar de un jugador reactivo a un jugador estratégico capaz de gestionar el restaurante de forma eficiente.

---

# 8. Onboarding

El onboarding se introduce progresivamente mediante las primeras jornadas.

### Día 1

- Una receta  
- Pocos clientes  
- Introducción al movimiento e interacción  

### Día 2–3

- Introducción de mejoras  
- Más clientes  

### Día 4+

- Nuevas recetas  
- Mayor complejidad  

El aprendizaje se basa en **experimentación directa**, evitando tutoriales invasivos.

---

# 9. Economía

## Ingresos

- Dinero por pedidos completados  
- Bonus por satisfacción alta  
- Bonus por día perfecto  

## Gastos

- Compra de estaciones  
- Mejora de equipos  
- Desbloqueo de recetas  

## Curva económica

Inicio → progreso rápido  
Medio → crecimiento moderado  
Final → optimización avanzada  

### Factores que afectan a los ingresos

Los ingresos obtenidos al final del día dependen de varios factores:

- Número de pedidos completados
- Rapidez en la entrega de pedidos
- Satisfacción global de los clientes
- Número de clientes que abandonan el restaurante

Esto incentiva a los jugadores a mejorar tanto la velocidad de trabajo como la organización del restaurante.

---

# 10. Framework MDA

El diseño del juego se analiza mediante el framework MDA (Mechanics, Dynamics, Aesthetics).

## Mecánicas

Las mecánicas son las reglas y sistemas que estructuran el juego:

- Movimiento de personajes
- Interacción con estaciones
- Preparación y entrega de pedidos
- Sistema de clientes y paciencia
- Colocación y mejora de objetos
- Gestión del tiempo de la jornada

## Dinámicas

Las dinámicas surgen de la interacción entre las mecánicas y los jugadores:

- Coordinación entre jugadores para dividir tareas
- Optimización del espacio del restaurante
- Gestión del estrés durante el servicio
- Adaptación a la dificultad creciente

## Estéticas

Las estéticas describen la experiencia emocional que el juego busca generar:

- Tensión durante el servicio
- Diversión cooperativa
- Satisfacción al optimizar el restaurante
- Sensación de progreso a lo largo de los días

---
