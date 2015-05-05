pmcputemp
====

*Leer en otro idioma: [Ingles](README.md), [Español](README.es.md).*

un ícono de estado de temperatura de cpu para el pobre

Construir
-----

ejecutar:

```
./configure
```

luego:

```
make
```

y como usuario root:

```
make install
```

Algunas opciones basicas para configurar `configure` son proporcionadas. Ejecute `configure --help`

Dependencias
-------
- Cairo
- Gtk+ >= 2.0 (rotos en gtk3 por ahora)
- Xlib

Uso
-----

Simplemente ejecute `pmcputemp` desde la linea de comandos, que lo hace aceptar un interruptor entero (1 - 10) para ajustar el retardo (5). 
Esto tratará de  generar un directorio de configuración y almacenamiento temporal `$HOME/.config/pmcputemp` en la primera ejecución. 
Ver el script `pmcputemp.sh`. En este directorio, `pmcputemprc` debe generarse con la ruta del archivo de la termperatura del cpu. 
En el caso de procesadores multi-núcleo, el primero núcleo es el que se obtiene. 
Esta es una limitación básicadel programa, despues de todo, los hombres y las mujeres pobres pueden tener dificultades 
para procurarse una maquina con procesadores multinúcleo. 
Los íconos con las lecturas se almacenan en este directorio y se escriben aproximadamente cada 5 (o el valor del interruptor) segundos. 

Errores
----
- Fahrenheit no soportados.
- El script podría no encontrar el archivo de la temperatura. Si sabes que tus sensores trabajan, 
usted puede ingresar la ruta manualmente, pero asegurese de que **no** habrá retorno.

Por favor reportar todos los errores aqui por ahora.
Traducciones son bienvenidas.
