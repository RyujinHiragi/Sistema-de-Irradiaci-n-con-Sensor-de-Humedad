# Sistema de Irradiación con Sensor de Humedad: Descripción Técnica

## Objetivo:
El objetivo de este sistema es automatizar el riego de un suelo mediante el monitoreo constante de la humedad utilizando un sensor capacitivo de humedad. Dependiendo de los datos proporcionados por el sensor, el sistema controla el encendido y apagado de una bomba de agua, además de mostrar una señal visual mediante un LED que indica el estado de la humedad.

## Componentes del Sistema:

1. **Microcontrolador (Arduino):**  
   Controlador principal que recibe la información del sensor de humedad y gestiona las acciones (encender/apagar la bomba de agua y el LED). El microcontrolador también se encarga de la lógica de control para activar el sistema de riego en función de la humedad del suelo.

2. **Sensor de Humedad (Sensor Capacitivo):**  
   Componente que mide la humedad del suelo a través de un cambio en su resistencia eléctrica. El sensor genera una señal analógica que es leída por el Arduino y comparada con un umbral predefinido (50%).

3. **LED Indicador:**  
   Dispositivo de salida que proporciona una señal visual sobre el estado de la humedad del suelo. Se enciende o apaga según el valor de humedad detectado por el sensor.

4. **Bomba de Agua:**  
   Dispositivo de salida controlado por el Arduino que activa el flujo de agua al suelo cuando la humedad está por debajo del umbral deseado (50%).

5. **Protoboard:**  
   Placa de pruebas donde se montan todos los componentes eléctricos del sistema para facilitar las conexiones y pruebas del circuito.

6. **Resistencias:**  
   Componentes pasivos utilizados para limitar la corriente y regular los voltajes en el circuito, evitando sobrecargas que puedan dañar los componentes.

7. **Multímetro:**  
   Herramienta utilizada para medir el voltaje, corriente y resistencia del sistema durante el proceso de configuración y monitoreo.

## Funcionamiento:

1. **Lectura de Humedad:**
   El sensor de humedad capacitivo mide continuamente la humedad del suelo. La señal analógica generada por el sensor es leída por un pin analógico del Arduino.

2. **Comparación y Lógica de Control:**
   El valor de humedad leído por el Arduino se compara con un umbral de 50%. Si la humedad es inferior al umbral, el sistema entra en modo de riego.

3. **Activación de la Bomba de Agua:**
   Si la humedad está por debajo del 50%, el Arduino activa una señal digital para encender la bomba de agua, utilizando un transistor o relé como interruptor para controlar el encendido de la bomba.

4. **Indicador LED:**
   Si la humedad está por debajo del 50%, el Arduino enciende el LED como indicador visual de que el sistema detectó que el suelo necesita riego. Si la humedad es superior al 50%, el LED se apaga.

5. **Desactivación del Sistema:**
   Cuando la humedad supera el umbral del 50%, el Arduino apaga el LED (indicando que la humedad está dentro de los niveles adecuados) y desactiva la bomba de agua para evitar el riego innecesario.

6. **Protección del Circuito:**
   Las resistencias se usan para regular los voltajes y evitar sobrecargas de corriente, protegiendo tanto al Arduino como a los demás componentes electrónicos del sistema. Estas resistencias se colocan según los requerimientos de cada componente.

7. **Monitoreo del Sistema:**
   Se utiliza un multímetro para verificar la correcta funcionalidad del sistema, asegurando que los voltajes y las corrientes estén dentro de los valores especificados para cada componente.

## Resumen del Ciclo de Operación:

1. El sensor de humedad mide el nivel de humedad del suelo.
2. El valor de humedad es procesado por el Arduino.
3. Si la humedad está por debajo del 50%, se enciende el LED y se activa la bomba de agua.
4. Si la humedad está por encima del 50%, el LED se apaga y la bomba de agua se detiene.
5. Las resistencias regulan el flujo de corriente para proteger el circuito.

Este sistema automatiza el riego del suelo, mejorando la eficiencia del proceso y reduciendo el consumo de agua, activándose solo cuando es necesario.
