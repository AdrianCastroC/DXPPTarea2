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

- Compra de ingredientes
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

# 11. Diseño del nivel (UD04)

## 11.1  Nivel seleccionado

El primer nivel jugable de **DISH DASH Restaurante Cooperativo** corresponde al **Día 1** del restaurante.

Esta jornada funciona como el primer contacto real con el bucle principal del juego: preparar pedidos, coordinar tareas, atender clientes y mantener la satisfacción global dentro de un espacio reducido.

Este planteamiento encaja con el GDD del proyecto, donde cada jornada funciona como un nivel independiente con dificultad progresiva, reinicio del día en caso de fracaso y mantenimiento del progreso global del restaurante.

### Tipo de estructura

La estructura del nivel es **funcional y secuencial**, organizada por áreas de trabajo conectadas entre sí.

Aunque el jugador puede desplazarse libremente por el restaurante, el diseño del nivel empuja a seguir una lógica clara de flujo de trabajo:

Entrada de clientes → asignación de mesa → preparación del pedido → cocinado → emplatado → entrega → limpieza o reorganización

Este enfoque se ajusta a lo trabajado en los apuntes de la unidad, donde se plantea dividir el nivel en áreas o burbujas que respondan a funciones concretas dentro del flujo de juego.

### División por áreas o burbujas

#### Entrada y cola de clientes
Es la zona por la que acceden los clientes al restaurante.  
Aquí comienza la presión del nivel, ya que marca el ritmo de llegada de pedidos.

#### Comedor
Espacio donde se sientan los clientes y esperan ser atendidos.  
Es una zona clave para la lectura del estado de la partida, porque permite identificar cuántos pedidos están pendientes y cuánto tiempo queda antes de que se agote la paciencia.

#### Zona de preparación
Área donde se reúnen ingredientes, platos y elementos necesarios para montar cada pedido.  
Sirve como espacio intermedio entre la recepción del pedido y su cocinado.

#### Zona de cocinado
Es el núcleo de trabajo principal del nivel.  
Aquí se realizan las acciones más críticas del servicio y es donde suelen generarse los mayores cuellos de botella.

#### Zona de entrega
Lugar desde el que el plato finalizado llega al cliente.  
Representa el cierre del ciclo principal de juego.

#### Zona de apoyo
Espacio destinado a fregadero, platos usados, apoyo logístico y reorganización rápida del entorno durante el servicio.

### Objetivo del nivel

El objetivo principal de este primer nivel es **completar con éxito la primera jornada del restaurante** manteniendo la satisfacción global en un rango seguro mientras se sirven correctamente los primeros pedidos.

### Objetivos concretos

- Atender a los primeros clientes antes de que pierdan la paciencia.
- Aprender el flujo básico de trabajo del restaurante.
- Preparar y entregar correctamente una receta inicial sencilla.
- Mantener la satisfacción general del restaurante.
- Finalizar la jornada sin colapso operativo.

### Obstáculos que impiden el progreso

En este nivel los obstáculos no son enemigos tradicionales, sino problemas derivados de la gestión y la coordinación.

#### Obstáculos principales

- Espacio reducido en cocina.
- Pocas estaciones de trabajo al inicio.
- Cruces constantes entre jugadores.
- Tiempo de espera limitado de los clientes.
- Posibilidad de equivocarse al entregar pedidos.
- Acumulación de tareas simultáneas.
- Equipamiento básico todavía poco eficiente.

Estos obstáculos están directamente relacionados con las mecánicas principales ya definidas en el GDD: preparación de platos, interacción con estaciones, sistema de espera de clientes, entrega de pedidos, satisfacción global y escalado progresivo de dificultad.

### Planificación del nivel

El nivel está diseñado con una progresión de intensidad creciente para enseñar al jugador a gestionar el caos de forma controlada.

#### Etapa 1 – Inicio controlado
Llegan pocos clientes, solo hay una receta básica y el jugador puede reconocer con claridad las distintas áreas del restaurante.  
La presión es baja y el foco está en comprender el flujo del servicio.

#### Etapa 2 – Aumento de carga
Comienzan a coincidir varias tareas al mismo tiempo.  
El jugador debe dividir mejor el trabajo y empieza a percibir que la cocina puede convertirse en un cuello de botella.

#### Etapa 3 – Pico de tensión
Se acumulan varios pedidos, la paciencia de algunos clientes baja con rapidez y la coordinación entre jugadores se vuelve imprescindible.  
Aquí aparece por primera vez la sensación real de caos cooperativo.

#### Etapa 4 – Resolución de jornada
Si el equipo ha gestionado bien el servicio, consigue estabilizar la situación, completar los últimos pedidos y cerrar la jornada con ingresos suficientes para seguir progresando.

### Elementos de ambiente o de script

A medida que avanza el nivel ocurren diversos eventos del sistema que ayudan a reforzar la sensación de servicio real y a comunicar el estado de la partida.

#### Elementos principales

- Entrada progresiva de clientes.
- Aparición visual de pedidos.
- Descenso de la barra de paciencia de cada cliente.
- Actualización de la barra global de satisfacción.
- Comentarios cortos de clientes al esperar o recibir el plato.
- Avisos visuales y sonoros cuando un pedido está cerca del fallo.
- Cierre automático de la jornada cuando termina el servicio.

Estos elementos responden a la fórmula explicada en la unidad: objetivos, obstáculos, situaciones y eventos programados dentro del nivel.

---

## 11.2 Características del nivel

### Entorno

El entorno del nivel es un **restaurante pequeño de inicio**, pensado para transmitir una sensación de negocio humilde pero funcional.

### Ubicación

La ubicación concreta es el **primer local del restaurante**, un espacio compacto que todavía no ha sido ampliado ni optimizado con mejoras avanzadas.

### Temática

La temática del nivel combina dos ideas principales:

- Inicio modesto de un proyecto gastronómico.
- Caos cooperativo en una cocina bajo presión.

El espacio debe comunicar que el restaurante todavía está en sus primeros días, por lo que su organización es básica, sus recursos son limitados y el margen de error es reducido.

### Tamaño del escenario

El escenario tiene un tamaño **reducido y controlado**.  
Esto permite:

- Evitar zonas vacías sin utilidad jugable.
- Facilitar la cooperación entre jugadores.
- Generar tensión mediante cruces y bloqueos.
- Hacer comprensible el espacio desde el primer momento.

Esta decisión sigue las recomendaciones de la unidad, que insiste en no crear espacios enormes sin interés mecánico y en diseñar escenarios proporcionados al tipo de juego y a la experiencia buscada.

### Interactividad

El nivel es altamente interactivo porque casi todo el espacio útil está relacionado con una acción de juego.

#### Elementos interactivos del nivel

- Fogones o cocina.
- Encimeras.
- Ingredientes.
- Platos.
- Mesas de clientes.
- Mostrador de entrega.
- Fregadero o zona de apoyo.

Cada elemento cumple una función dentro del circuito principal del restaurante, reforzando la idea de que el escenario no es un simple decorado, sino una parte activa del sistema jugable. Esta idea también aparece en la unidad cuando se indica que el escenario debe tratarse como un elemento conectado con las mecánicas y la experiencia del jugador.

### Puntos de referencia del nivel

Los puntos de referencia son fundamentales para que el jugador se oriente y lea rápidamente el espacio.

#### Puntos focales principales

- Cocina principal.
- Mostrador de entrega.
- Comedor.
- Entrada de clientes.

Estos puntos ayudan a identificar con rapidez dónde se genera cada parte del flujo del servicio y sirven como referencia visual durante los momentos de mayor tensión.

### Ritmo del nivel

El ritmo del primer nivel sigue una curva sencilla y progresiva:

- Inicio tranquilo.
- Incremento gradual de presión.
- Pico de caos controlado.
- Cierre y recompensa.

Esto permite introducir la experiencia central del juego sin saturar al jugador desde el primer minuto.

### Proporción y circulación

La circulación del espacio está diseñada para provocar cooperación, pero también pequeños conflictos de movimiento que obliguen a mejorar la organización del equipo.

Los desplazamientos son cortos, pero las trayectorias se cruzan con frecuencia, generando situaciones donde la distribución del trabajo y el posicionamiento dentro del espacio resultan tan importantes como la propia receta.

---

# 12. Referencias visuales

### Inspiración principal

El diseño del primer nivel se inspira principalmente en referentes de juegos cooperativos de cocina y gestión, así como en espacios reales de restauración compacta.

### Referencias de videojuegos

#### Overcooked
Aporta una referencia clara en cuanto a:
- lectura rápida del espacio,
- distribución por zonas funcionales,
- caos cooperativo,
- necesidad de coordinación constante.

#### PlateUp!
Aporta inspiración en:
- organización del restaurante,
- optimización del layout,
- importancia de la colocación de objetos,
- progresión del local entre jornadas.

Estas referencias ya estaban recogidas en el GDD base del proyecto y siguen siendo las más adecuadas para orientar el diseño del nivel inicial. 

### Referencias espaciales y artísticas

Además de los referentes jugables, el nivel toma inspiración de:

- cocinas industriales pequeñas,
- restaurantes de comida rápida con distribución compacta,
- planos cenitales de locales de restauración,
- espacios donde cocina y comedor están muy próximos,
- diseños visuales cálidos para comedor y neutros para cocina.

### Intención visual del nivel

Visualmente, el primer nivel debe transmitir:

- restaurante pequeño,
- entorno legible,
- sensación de actividad constante,
- espacio acogedor pero limitado,
- contraste entre zona de clientes y zona de trabajo interno.

### Art Bible del nivel

La Art Bible del primer nivel se basa en estos principios:

- Lectura clara desde cámara cenital o isométrica.
- Separación visual entre cocina y comedor.
- Colores cálidos para la zona de clientes.
- Colores más neutros o fríos para la cocina.
- Objetos grandes y reconocibles para facilitar la legibilidad.
- Diseño visual coherente con una experiencia cooperativa rápida y accesible.

---

# 13. Elementos del nivel

### Listado 1 – Assets y objetos del escenario

#### Estructuras y mobiliario
- Paredes del restaurante
- Suelo de cocina
- Suelo de comedor
- Puerta de entrada
- Mesas
- Sillas

#### Equipamiento de cocina
- Fogón o cocina
- Encimeras
- Fregadero
- Nevera
- Zona de platos
- Superficie de apoyo

#### Elementos visuales de ambiente
- Lámparas
- Decoración básica del comedor
- Carteles o menú
- Caja registradora
- Elementos decorativos simples del local

### Listado 2 – Elementos jugables y sistémicos

#### Elementos de cliente
- Cliente estándar
- Paciencia individual
- Pedido visible
- Estado de satisfacción

#### Elementos de servicio
- Plato preparado
- Pedido correcto
- Pedido incorrecto
- Tiempo de espera
- Entrega completada

#### Elementos de sistema
- Barra global de satisfacción
- Temporizador de jornada
- Ingresos del día
- Fin de jornada
- Reinicio del día en caso de fracaso

### Listado 3 – Obstáculos y presión del nivel

#### Obstáculos espaciales
- Cocina estrecha
- Cruces entre jugadores
- Poca separación entre estaciones

#### Obstáculos temporales
- Paciencia limitada
- Acumulación de pedidos
- Tiempo de servicio ajustado

#### Obstáculos operativos
- Equipamiento lento
- Errores de coordinación
- Mala asignación de tareas
- Saturación del espacio de trabajo

### Listado 4 – Recompensas y progresión

#### Recompensas del nivel
- Dinero por pedidos completados
- Bonus por satisfacción alta
- Bonus por completar bien la jornada

#### Recompensas de progresión
- Mejora de equipamiento
- Compra de nuevas estaciones
- Optimización futura del restaurante
- Posibilidad de afrontar jornadas posteriores con mejor eficiencia

---

# 14. Música y sonido

### Función del sonido en el nivel

El sonido en el primer nivel tiene una función doble:

- comunicar información útil al jugador,
- reforzar la atmósfera de restaurante activo y cooperativo.

La unidad indica que deben clasificarse los sonidos por familias y diseñarse un mapa sonoro teniendo en cuenta el audio listener, las fuentes de sonido y las posibles zonas de reverberación.

### Familias de sonido del nivel

#### DX – Diálogo
Corresponde a las voces o expresiones verbales del juego.

Ejemplos:
- frases cortas de clientes al entrar,
- quejas cuando esperan demasiado,
- expresiones de satisfacción al recibir el plato,
- avisos breves del sistema de jornada.

#### MX – Música
Corresponde a la música de fondo del nivel.

Ejemplos:
- música base suave y dinámica durante el servicio,
- aumento de intensidad en momentos de mayor presión,
- música de final de jornada en función del resultado.

#### SFX – Efectos de sonido
Sonidos asociados a objetos, acciones y eventos del sistema.

Ejemplos:
- sonido de cocinar,
- sonido de servir platos,
- sonido de caja registradora,
- aviso de pedido completado,
- aviso de error,
- temporizador o señal de urgencia.

#### FOL – Foley
Sonidos generados directamente por las acciones del jugador.

Ejemplos:
- pasos de los cocineros,
- coger y soltar platos,
- manipular ingredientes,
- abrir o cerrar elementos del mobiliario,
- desplazamiento rápido por cocina.

#### BG – Fondos de ambiente
Sonidos ambientales que dan vida al espacio.

Ejemplos:
- murmullo de comedor,
- ruido suave de cocina,
- ventilación,
- ambiente general del local,
- sonido exterior tenue si se percibe desde la entrada.

### Mapa sonoro del nivel

### Audio Listener
El audio listener debe situarse en la cámara principal compartida, ya que representa el punto general desde el que el jugador percibe el entorno durante la jornada.

### Fuentes de audio principales

#### Fuentes 2D
Se utilizarán para sonidos no dependientes de posición concreta:
- música de fondo,
- avisos globales del sistema,
- interfaz sonora,
- algunos refuerzos de feedback.

#### Fuentes 3D
Se utilizarán para sonidos ligados al espacio físico del restaurante:
- fogones,
- fregadero,
- caja registradora,
- entrada del local,
- zona de clientes,
- área de entrega.

### Zonas del mapa sonoro

#### Entrada
Sonidos suaves de puerta, llegada de clientes y transición desde el exterior.

#### Comedor
Murmullo de clientes, pequeños comentarios y ambiente general de restaurante.

#### Cocina
Zona con mayor densidad sonora:
- cocinado,
- utensilios,
- pasos,
- preparación,
- sonidos de trabajo repetidos.

#### Entrega
Pequeños sonidos de confirmación al servir correctamente y refuerzo auditivo de cierre de pedido.

### Reverberación

En el primer nivel no es necesario exagerar el uso de reverberación, pero sí puede contemplarse una ligera diferencia entre cocina y comedor para reforzar la sensación de espacio interior dividido.

### Objetivo del diseño sonoro

El objetivo sonoro del nivel es:

- hacer comprensible el estado del servicio,
- reforzar la presión temporal,
- mejorar la inmersión,
- dar feedback inmediato al jugador,
- evitar saturación auditiva manteniendo claridad en los sonidos importantes.

Esto se alinea con lo indicado en la unidad sobre la utilidad del sonido para transmitir acciones, estado del entorno, atmósfera y progreso del jugador.

---
