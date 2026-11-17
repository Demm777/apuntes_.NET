# AGENTES DE INGENIERIA EN REQUISITOS CON IA
## modelado de negocio
###  diagramas de uso del caso del negocio
**muñeco con linea:** actores del negocio
<br>
**circulo:** procesos del negocio
![Diagrama](https://www.researchgate.net/publication/266316706/figure/fig6/AS:651890572402690@1532434232472/Figura-73-Diagrama-de-casos-de-uso-de-negocio-para-el-sistema-del-hotel.png)

## Herramientas
* notebooklm
  > promp maestro <br>
  > harness

## definicion del proyecto
- ponerse de acuerdo <br>

### genera
- requisitos funcionales
- r/no funcionales

## Estructura del prompt
### contexto
informacion que debe tener la ia antes de iniciar
### intencion
objetivo especifico del trabajp
### loop
mecanica de conversacion hasta llegar a lo requerido
### harness
seguridad que evita errores y mejora la calidad del mensaje

## Trabajo en Notebook lm:
1. ### crear cuaderno (Metodologia de requerimientos)
2. ### agregar las fuentes
      1. ### normas ISO (ingenieria en requerimientos)
   1. ### diden 
   2. ### babok
   3. ### manual itil (interaccion guiada)
   4. ### fuentes para llenar con informacion 
      - frm-001 identificacion de necesidades
      - stakeholder
      -  objetivos de negocio
3. ### agregar prompts
- ### prompt 1:
```
te acabo de entregar los documentos para la construcción de los documento necesarios para un proceso de ingeniería de requerimientos con base en una pequeña metodología que hemos diseñado dentro de un proceso de formación. la guía metodológica se encuentra en el documento FMR_000_Guia_Metodologica_Requisitos, revísalo y cuando estés listo me informas para darte un prompt especializado para la captura de información y diligenciamiento de cada formato
```
- ### prompt 2:
```
Actúa como un Ingeniero Senior de Requerimientos de Software y Analista de Negocio. 
OBJETIVO 
Construir el documento FMR_001 - Identificación de Necesidades. 
Debes identificar el problema de negocio, las necesidades y los objetivos que justifican el desarrollo de una solución de software. 
IMPORTANTE 
- No recopiles requisitos funcionales.
- No hables de módulos.
- No hables de pantallas.
- No hables de tecnología.
- Enfócate únicamente en comprender el problema y la necesidad.
 MODO DE TRABAJO 
El flujo inicia únicamente cuando el usuario escriba: 
iniciar 
Responde exactamente: 
"Entendido. Iniciando identificación de necesidades." 
CAPTURA GUIADA 
Realiza una única pregunta por interacción. 
Orden de captura: 
1. Nombre del proyecto
2. Organización
3. Área solicitante
4. Responsable de la iniciativa
5. Problema actual
6. Impacto del problema
7. Necesidad identificada
8. Objetivos de negocio
9. Beneficios esperados
10. Indicadores de éxito
11. Restricciones iniciales 
Después de cada respuesta: 
1. Validar información.
2. Resumir lo capturado.
3. Formular la siguiente pregunta. 
No avanzar si la respuesta es insuficiente o ambigua. 
Al finalizar: 
Generar un resumen estructurado. 
Solicitar confirmación. 
No cerrar la fase hasta que el usuario apruebe la información. 
SALIDA ESPERADA 
Documento FMR_001 consolidado.
```
4. ### llenar informacion desde el promt anterior
5. ### prompts:
```
Actualmente el centro de automatización industrial no cuenta con una estrategia claramente definida para la solicitud, registro y seguimiento para las solicitudes de servicios de soporte en el área de tecnologías de la información, esta situación ocasiona que los servicios no se presten oportunamente e incluso algunos servicios dejan de ser atendidos y esto conlleva a perdidas debido a tiempos de inactividad de varios trabajadores
```
6. 
```
los impactos son:

1. perdidas economicas por inactividad laboral

2. incremento en el deterioro de los activos informaticos

3.. baja percepcion de la calidad del servicio 
```
7. 
```
Se requiere implementar un mecanismo eficiente por medio del cual se pueda realizar, el registro, actualización y generación de reportes de la totalidad de servicios tecnológicos solicitados por los usuarios
```
8. 
```
1. Registrar la totalidad de los incidentes presentados en los activos de TI. 2. Mejorar cobertura en la prestación de servicios. 3. Disminuir los tiempos de atención. 4. Incrementar los tiempos de actividad laboral de los usuarios. 5. Incrementar el tiempo de vida util de los activos informaticos
```
9. 
```
1. Optimizar el presupuesto del área de TI. 2. Incrementar el tiempo de operatividad de los equipos informáticos. 3. Incrementar los indicadores de continuidad del servicio. 4. Disminuir los procesos de baja para equipos electrónicos
```
10.
```
1. cantidad de servicios atendidos. 2. Disminución del presupuesto operativo del área de TI.  3. Disminución de procesos de chatarrización de equipos
``` 
11. ### terminado (descargar archivo FRM_001)
## 2da fase, continuar prompt scrunt
```
Actúa como Analista Senior de Negocio. 
OBJETIVO 
Construir el documento FMR_002 - Identificación y Análisis de Stakeholders. 
Debes utilizar la información obtenida en FMR_001. 
MODO DE TRABAJO 
El flujo inicia únicamente cuando el usuario escriba: 
iniciar 
CAPTURA GUIADA 
Realiza una pregunta por interacción. 
Identificar: 
1. Patrocinador
2. Cliente
3. Usuarios principales
4. Usuarios secundarios
5. Administradores 
Para cada stakeholder capturar: 
- Nombre
- Rol
- Interés
- Nivel de influencia
- Necesidades
- Participación en el proyecto 
Nunca pases al siguiente stakeholder sin completar el actual. 
Al finalizar: 
Generar una matriz de stakeholders. 
Solicitar aprobación. 
SALIDA ESPERADA 
Matriz completa de stakeholders.
```
- ### agregar stakeholders
    > patrocinador <br>
    > cliente 1  <br>
    > cliente 2  <br>
    > usuarios principales  <br>
    > usuarios secundarios  <br>
    > administradores  <br>
- ### descargar archivo FRM_002
## FRM_003 - Alcance
1.
```
El centro de automatización industrial del Sena regional Caldas, necesita el desarrollo de un sistema de información por medio del cual se pueda realizar la gestión de la prestación de servicios tecnológicos que solicitan diariamente los usuarios los funcionarios del centro.
```
2.
```
adicionemos lo siguiente: el sistema no tendrá dependencias con aplicaciones externas para la realización de tareas de mantenimiento ni de inventario de hardware, tampoco entregará información a otras aplicaciones, todo se limita a lo que se definió en la fase alcance incluido
```
## Objetivos de negocio:
1.
```
Falta de trazabilidad en la atención de solicitudes de soporte, tiempos prolongados de respuesta sin control de SLA, dificultad para auditar el estado real de los activos informáticos y sus componentes, falta de control en el vencimiento de licencias y garantías, o dispersión de la información de mantenimiento preventivo
```
secion 1 terminada
