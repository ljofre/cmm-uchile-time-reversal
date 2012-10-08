Proyecto con la estimación de la fuente por medio del conjunto de set de datos
entregados por codelco:

#Instrucciones

1. Bajar el proyecto mediante un archivo zip o crear un clone del proyecto
2. En Matlab agregar la descargada o clonada en el **Path** del sistema
3. Ejecutar los siguientes scripts de Matlab

##Obtensión de la forma de la fuente asumiendo un punto conocido

 ```
Events = importEvents();             % Importa todos los archivos a una lista de objetos events
n = 2;                               % Número del evento que se desea estimar la forma de la fuente
event = Events(n);                   % Evento en estudio, puede ser en 1:event.count
                                     % forma de la fuente y error de estimación
nSync = 750;
nSrc = 250;
dt = 0.0000025;
[src, cutsrc, filtsrc, filtcutsrc, error] = source(event, nSync, nSrc, dt); 
```
Para obtener el vector perpendicular al plano de ruptura se puede hacer el cambio de base
mediante una matriz ortogonal que produzca máximo desplazamiento en un eje

```        
[rotateSrc , B] = ChangeOfBasis(src) % rotaci'on del campo de desplazamiento de la fuente
                                     % para encontrar el plano de ruptura y la matriz de cambio de base B
plot(rotateSrc);
 ```
En el cual veremos el campo de desplazamiento

##Pruebas de validez del código 
 
Este framework consta de una serie de pruebas que validan la integridad numérica de los resultados de las mediciones reales.
### Prueba sobre la estimación numerica de la fuente por medio de mínimos cuadrados
### Pruebas sobre la inversión de una señal sintética


### Inversión de la señal

<<<<<<< HEAD
### Busqueda del punto de ruptura
 
 
=======
### Busqueda del punto de ruptura
>>>>>>> 4a93fb221ba8fb9c7293abb27d05cc639f0e3152
