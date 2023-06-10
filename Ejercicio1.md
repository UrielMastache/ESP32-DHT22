# Practica ESP32 con DHT22
Este repositorio muestra como podemos programar una ESP32 con el sensor DHT22.

## Introducción

### Descripción

La ```Esp32``` la utilizamos en un entorno de adquision de datos, lo cual en esta practica ocuparemos un sensor (```DTH22```) para adquirir temperatura y humedad del entorno; Cabe aclarar que esta practica se usara un simulador llamado [WOKWI](https://https://wokwi.com/).


## Material Necesario

Para realizar esta practica necesitas lo siguiente

- [WOKWI](https://https://wokwi.com/)
- Tarjeta ESP 32
- Sensor DHT22
- Y muchas ganas de chambear


## Instrucciones

### Requisitos previos

Para poder usar este repositorio necesitas entrar a la plataforma [WOKWI](https://https://wokwi.com/).


### Instrucciones de preparación de entorno 

1. Abrir la terminal de programación y colocar la siguente programación:



```
#include "DHTesp.h"


const int DHT_PIN = 15;
DHTesp dhtSensor;


void setup() {

  Serial.begin(115200);
  dhtSensor.setup(DHT_PIN, DHTesp::DHT22);
}

void loop() {

  TempAndHumidity  data = dhtSensor.getTempAndHumidity();
  Serial.println("Temp: " + String(data.temperature, 1) + "°C");
  Serial.println("Humidity: " + String(data.humidity, 1) + "%");
  Serial.println("---");
  delay(1000);
  
}



```
3. Instalar la libreria de **DHT sensor library for ESPx** como se muestra en la siguente imagen.

![](https://github.com/UrielMastache/ESP32-DHT22/blob/main/Descargando%20libreria%20para%20sensor.png?raw=true)

3. Hacer la conexion de **DHT11** con la **ESP32** como se muestra en la siguente imagen.

![](https://github.com/UrielMastache/VisualCodePracticas/blob/main/Captura%20de%20pantalla%20(4).png?raw=true)

### Instrucciónes de operación

1. Iniciar simulador.
2. Visualizar los datos en el monitor serial.
3. Colocar la temperatura y humedad dando *doble click* al sensor **DHT22** 

## Resultados

Cuando haya funcionado, verás los valores dentro del monitor serial como se muestra en la siguente imagen.

![](https://github.com/UrielMastache/VisualCodePracticas/blob/main/Simulaci%C3%B3n%20ESP32%20con%20Sensor%20de%20temp%20y%20humedad.png?raw=true)

## Comentarios

De igual manera ya que estas simulando el archivo, dandole clic al sensor DHT22 puedes modificar los valores de humedad y temperatura, y también se modificaran en tiempo real en la pantalla de visualización de la parte de abajo (como se muestra a continuación).

![](https://github.com/UrielMastache/VisualCodePracticas/blob/main/Simulaci%C3%B3n%20cambiando%20valores%20de%20sensor.png?raw=true)

Gracias por ver :D 

Ciao.