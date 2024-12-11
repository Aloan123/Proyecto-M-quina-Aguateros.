# Proyecto-Máquina-Aguateros.
Modelo de simulación de una máquina de aguateros ubicada en la universidad de los Andes.

## Construido con.
- TIA PORTAL (V.17)
- PLCSIM (V.17)
- RUN TIME ADVANCE (Versión por defecto dentro del TIA PORTAL V.17)

* TIA PORTAL ya viene con todo lo anterior si así se indica en el proceso de instalación.

## Instalación del proyecto.
- Abrir el archivo .zip presente en este repositorio
  Proyecto_máquina_aguateros.zip
- Entrar a la carpeta Proyecto_máquina_aguateros -
- Correr el programa Proyecto_máquina_aguateros (.p17)
? Dar doble click en el proyecto dentro del TIA PORTAL (si así lo pide)
- Ir a Start > Proyect view > open proyect view
? Desplegar Proyecto_máquina_aguateros (si así lo pide)

* Se debe simular cada módulo del proyecto por aparte y luego la lógica de el módulo PLC
  se sincroniza con la simulación del módulo PC[HMI]

## Simular Módulo PLC
- Dar click sobre el módulo PLC_1 [CPU1214/DC/DC/Rly]
- Click derecho > Compile > Software (Rebuild all)
? Click derecho > Compile > Hardware (Rebuild all)  (de ser necesario)
- Pulsar sobre la opción "start simulation", para correr la simulación                (Loading...)
- En "Establish connection to device" > Pulsar > consider as trusted and m...          (Loading...)
- En "Load results" > Pulsar en > Load
- En "Load results" > Pulsar en > Start Modules > Start module
- Pulsar en > Finish

? Para inspeccionar cambios > Desplegar > módulo PLC > Program Blocks > Main [OB1]

## Abrir la tabla de forzado de variables
- Dentro de PLCSIM > Pulsar en > Switch to project view                              (Loading...)
- Dentro de Project view > Pulsar en > Project > new > create                         (Loading...)
- Pulsar en > Nombre del proyecto > SIM tables > SIM table_1
- Pulsar en celda name > Escribir nombre de variable "UI" (User interface)
- Pulsar en nueva celda name > Escribir nombre de variable "MI" (Machine interface)
- Pulsar en nueva celda name > Escribir nombre de variable "Pago"    (Acción de pagar al banco)
- Pulsar en nueva celda name > Escribir nombre de variable "Servir"   (Acción de servir el tipo de agua)
- Pulsar en nuve celda name > Escribir nombre de variable "Clima"  (Tipo de pago)
- Pulsar en nuve celda name > Escribir nombre de variable "Frío"   (Tipo de agua)
- Pulsar en nuve celda name > Escribir nombre de variable "Gas"    (Tipo de agua)
  
## Simular Pantalla PC > HMI
- Desplegar > PC-System_1 [SIMATIC PC station]
- Desplagar > HMI_RT_2 [WinCC RT Advanced]
- Deplegar > Screens > Screen_1
- Pulsar en > Screen_1
- Pulsar sobre la opción "Start RunTime on the PC", para correr la pantalla de simulación     (Loading...)

## Correr el modelo de simulación
- Luego de tener simulado el Módulo PLC y el Módulo PC[HMI]
- Pulsar sobre > programa PLCSIM
- Pulsar en ópcion "float" (separar ventana de variables de la vista del proyecto)
- Pulsar sobre > programa WINCCRA
- Pulsar windows > escoger programa PLCSIM
- Ubicar la ventana de variables a un lado de la pantalla de simulación (para ser claro a simple vista)

* Activar y desativar check-boxes de las respectivas variables para activar/desactivar procesos dentro
  del modelo de simulación.
