# Cthangover: Starter Party — con quién empieza el jugador

Este mod pequeño da a una partida nueva de Cthangover su estado inicial: Marao en el grupo y la habilidad Tratante de esclavos en la colección de habilidades. Solo contiene ese código; el personaje y la habilidad en sí son datos del juego base y del motor de habilidades.

## Qué tiene un jugador nuevo

El panel de personajes al comienzo de Cthangover: un miembro del grupo, Marao, con dos acciones y un hueco libre:

![El panel de acciones del personaje: Grupo 1, Marao (plantilla 2, HP 16/16, PA 1, ATK 5, DEF 0) con Ataque básico y Defensa, y un tercer hueco vacío.](assets/party.jpg)

El panel de habilidades: una sola habilidad, Tratante de esclavos:

![El panel de habilidades: la colección tiene una habilidad pasiva épica, Tratante de esclavos, "+10 % de probabilidad de reclutar", con la descripción "Permite esclavizar a un enemigo derrotado con una probabilidad base del 10 %. La manutención del esclavo corre de tu cuenta." y el efecto de colección +10 % de probabilidad de reclutar.](assets/skills.jpg)

Tratante de esclavos es lo que permite al jugador capturar enemigos derrotados (ver Recruiting): sin él ningún enemigo puede unirse.

## Cuándo actúa

- Cuando los mods del juego están listos, el mod añade el personaje `Marao` al grupo y concede la habilidad `slave_master`.
- Cada vez que empieza una **partida nueva** lo hace otra vez, porque una partida nueva primero vacía el grupo.
- Cargar una partida guardada sustituye el grupo y las habilidades por los guardados. Ambos pasos pueden ejecutarse más de una vez sin problema: Marao no se añade dos veces ni la habilidad se concede dos veces.

## Cómo cambiar el inicio

- Otro mod puede añadir más personajes iniciales igual: un inicializador en C# que añade sus personajes al grupo cuando los mods están listos.
- Para empezar sin Marao o sin la habilidad, deja este mod fuera de la colección del juego y siembra el grupo en tu propio mod.

## Problemas conocidos

- La carta de Tratante de esclavos no tiene imagen: falta la imagen de la habilidad.
- La carta y su descripción prometen "+10 % de probabilidad de reclutar", pero ningún código lee ese bono; la tirada de captura usa solo la probabilidad propia del enemigo.
