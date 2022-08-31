> # Flow4-NodeRed

Este repositorio contiene el Flow4 del curso de NodeRed, visto en los contenidos del curso Internet de las cosas impartido por Código IoT.

## Introducción

A continuación se desarrollará un Flujo a través de Node-RED, en el cuál se hará uso de los nodos MQTT, JSON, Function, Gauge y Chart, con estos tendremos como resultado la facilidad de observar un gráfico que obtiene valores a través del nodo MQTT.
  
## Material Necesario

Para realizar este flow necesitas lo siguiente

-   [Ubuntu 20.04](https://releases.ubuntu.com/20.04/)
-   [NodeJS](https://nodejs.org/es/)
    -   [NPM](https://www.npmjs.com/)
    -   [NodeRed](https://nodered.org/docs/getting-started/local)

## Material de referencia

En los siguientes enlaces puedes encontrar cursos en la plataforma de edu.codigoiot.com que te permitirán realiar las configuraciones necesarias

-   [Instalación de Virutal Box y Ubuntu 20.04](https://edu.codigoiot.com/course/view.php?id=812)
-   [Instalación de NodeRed](https://edu.codigoiot.com/course/view.php?id=817)
-   [Introducción a NodeRed](https://edu.codigoiot.com/course/view.php?id=278)

## Instrucciones

### Requisitos previos

1.  Instalación de NodeJS. Se recomienda tener instalado NodeJS en alguna versión LTS. Al momento de creación de este documento, se usó la versión 16.17.0LTS. Esta instalación debe incluir las Build-Tools para hacer uso de NPM
2.  Instalación de NodeRed. La instalación se realiza por NPM. Al momento de la creación de este contenido, se usó la versión 3.0.2
Para desarrollar el flujo será necesario el uso de los siguientes nodos.



### Instrucciones de preparación del entorno

Para ejecutar este flow, es necesario lo siguiente

1.  Arrancar NodeRed con el comando  `node-red`

## Pasos a seguir

*Para que este flow funcione, debes cumplir con los siguientes requisitos previos.*

**Nodos necesarios**

-   MQTT
    -    `MQTT Input`entrada o el `MQTT Output`nodo y un `MQTT Config`nodo asociado para conectarse a un intermediario MQTT. En este caso solo usaremos el nodo `MQTT Input`.
 - JSON
     -   Realizan acciones con la información y traspasan los datos resultantes de dicha acción a los nodos siguientes con los que está enlazado a través de su puerto o puertos de salida.
- FUNCTION
	- Permite la incorporación de código **_Node.js_** propio ('custom code') para el tratamiento de los datos recibidos o realizar acciones especializadas. 
- GAUGE
	-  Gráfico en forma de Gauge para mostrar una aguja móvil.
- CHART
	- El nodo de gráfico se utiliza para mostrar datos de entrada en varias formas de gráfico (línea, pastel, barra, etc.).


1.- Arrastrar al espacio de trabajo el número de nodos que se muestran a continuación:
| NODO | CANTIDAD  |
|--|--|
|MQTT| 1 |
|JSON|1|
|FUNCTION|2|
|GAUGE|2|
|CHART|1|
2.- Conexión de los nodos, conectar el nodo mqtt-in>nodo json>nodo function temp & function hum posteriormente cada uno de los nodo function se conectaran con su propio nodo gauge, finalmente el nodo chart se conectara directamente con los nodos function. 
![Conexión de nodos.](https://github.com/DafneJimenezR/Flow4-NodeRed/blob/main/conexiones.png)
3.- Abrir la sección de dashboard crear un nuevo tab con el nombre Flow 4 - MQTT y crear tres grupos uno con el nombre Temperatura y Humedad
![](https://github.com/DafneJimenezR/Flow4-NodeRed/blob/main/dashboart_layout.png)
4- Configuración de los nodos
MQTT
![](https://github.com/DafneJimenezR/Flow4-NodeRed/blob/main/mqtt_in.png)

JSON
![](https://github.com/DafneJimenezR/Flow4-NodeRed/blob/main/json_.png)

FUNCTION-Temperatura
![](https://github.com/DafneJimenezR/Flow4-NodeRed/blob/main/function_temp.png)

FUNCTION-Humedad
![](https://github.com/DafneJimenezR/Flow4-NodeRed/blob/main/function_hum.png)

Gauge-Temperatura
![](https://github.com/DafneJimenezR/Flow4-NodeRed/blob/main/gauge_temp.png)

Gauge-Humedad
![](https://github.com/DafneJimenezR/Flow4-NodeRed/blob/main/gauge_hum.png)

Chart
![](https://github.com/DafneJimenezR/Flow4-NodeRed/blob/main/chart.png)

### Instrucciones de operación
1. Guardar el flow oprimiendo el botón  **Deploy**
2. Para observar el resutlado de este flow, abre un navegador y dirígete a localhost:1880/ui

## Resultados

A continuación puedes ver los nodos del flow.

[![](https://github.com/DafneJimenezR/Flow4-NodeRed/blob/main/nodos.png)](https://github.com/DafneJimenezR/Flow4-NodeRed/blob/main/nodos.png

A continuación puede ver el tablero resultante.
[![](https://github.com/DafneJimenezR/Flow4-NodeRed/blob/main/tablero.png)](https://github.com/DafneJimenezR/Flow4-NodeRed/blob/main/tablero.png)

## Evidencias

-   [Repositorio](https://github.com/DafneJimenezR/Flow2-NodeRed)

## Créditos
Creado por  [DafneJimenezR](https://github.com/DafneJimenezR)



