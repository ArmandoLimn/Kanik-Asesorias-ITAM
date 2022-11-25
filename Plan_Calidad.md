## 1. Identificadores del plan de calidad

Versión: 1.0 

Autores: 

+ Mauricio de Ariño
+ Armando Limón
+ Yhoaly Lorena Mondragón
+ Arturo Liera Bravo

Última edición: 24 de noviembre de 2022

## 2. Referencias

Este documento está basado en los estándares de calidad del IEEE-829 y en el SRS que puede ser consultado [aquí](https://github.com/ArmandoLimn/Kanik-Asesorias-ITAM).

## 3. Introducción

Se va a probar la correcta implementación del software en la página de AsesoríasITAM.
* Validaciones del sistema 
* Funcionalidades relacionadas con la Base de datos
* UI de cada pantalla

## 4. Funcionalidades a probar

* Creación de cuentas
* Inicio de sesión 
* Navegación por interfaz
* Carga de archivos


## 5. Riesgos del Software

* No implementamos medidas de seguridad dentro de la aplicación, solo en la creación de cuentas.
* Se pueden iniciar múltiples sesiones distintas en un mismo navegador
* Dependemos de AWS
* regargar

## 6. Pruebas que se van a realizar
Funcionamiento de la aplicación en general.

## 7. Pruebas que no se van a realizar

* Funcionamiento de la aplicación desde la perspectiva del administrador, ya funciona correctamente
* Agregar y quitar notas, no estará disponible en esta versión del software

## Estrategia de las pruebas

Se harán pruebas a la aplicación con la estrategia Grey Box Testing, aplicando principalmente la técnica de regression testing para identificar rápidamente qué es lo que no está funcionando y si es un problema del código o de un mal uso de la aplicación.

Los pasos a seguir son:

1. Seleccionar inputs.
2. Identificar outputs que deberían salir.
3. Identificar subfuncionalidades relacionadas con la prueba
4. Desarrollar inputs y outputs prueba para las subfucionalidades
5. Hacer casos prueba para las subfuncionalidades
6. Verificar el resultado de las subfuncionalides
7. Repetir pasos 3 a 6 para el resto de subfucionalidades
8. Hacer pruebas con la funcionalidad completa.

## 9. Criterios de éxito y fracaso
| Funcionalidad     | Escenario   | Semáforo      |
|-------------------|-------------|---------------|
| Creación de cuentas     | Creo una cuenta con correo del ITAM y otra con correo externo                                       | Verde    |
| Inicio de sesión        | Al introducir mis credeciales pienso que tengo un error y doy clic en la lupa para ver si voy bien  | Amarillo |
| Navegación por interfaz | Navego entre las distintas pestañas con facilidad                                                   | Amarillo |
| Búsqueda de grupos      | Busco grupos para la materia Contabilidad I                                                         | Verde    |
| Creación de grupos      | Al crear un grupo quiero poner una foto de mi horario                                               | Rojo | 
| Suscripción a grupos    | Me inscribo a un grupo por accidente y lo quiero dar de baja                                        | Verde |

## 10. Criterios de suspensión y de reanudación de pruebas

* Suspensión: La funcionalidad no presenta fallos en el uso que un usuario le daría contando posibles accidentes como introducir datos erróneos en campos.
* Reanudación: La funcionalidad presenta un fallo crítico que evita el uso de la plataforma.

## 11. Entregables de las pruebas

* Documento de plan de calidad
* Resultados de las pruebas
* Especificación del diseño de cada prueba
* Error logs
* Reporte de los problemas encontrados y soluciones propuestas

## 12. Pruebas pendientes

* Probar funcionalidad de añadir y quitar archivos
* Probar cambios en sección de Ajustes

## 13. Necesidades extra del ambiente

Para realizar las pruebas se proporcionará una base de datos inicial para experimentar y cuentas para realizar las pruebas.

## 14. Necesidades de equipo y entrenamiento
* Se va a dar acceso a la base de datos de prueba
* Se requiere haber leído el documento README de este proyecto que se puede encontrar [aquí](https://github.com/Asesorias-ITAM/AsesoriasITAM/blob/main/README.md)
* Se va a proporcionar una versión del código para realizar las pruebas y realizar cambios sin modificar inmediatamente el código principal

## 15 Responsabilidades

+ Yhoaly Mondragón, está a cargo y es quién decide decide tanto los riesgos del proyecto como el alcance de las pruebas.
+ Arturo Liera dará el entrenamiento para utilizar la aplicación y será quien proporcionará los elementos para realizar las pruebas.
+ Armando Limón se encargará de diseñar las pruebas y organizar tiempos para realizarlas.
+ Mauricio de Ariño tomará las decisiones sobre cualquier cosa que no esté escrita en este plan de calidad

## 16. Itinerario
Al estar usando la metodología Cascada, las pruebas se realizarán al término de su implementación.

## 17. Riesgos planeados
* Tenemos un equipo limitado por lo que debemos trabajar lo mejor posible alrededor de los requerimientos
* Ante un tiempo prolongado en el desarrollo de una feature, se reducirá el tiempo de pruebas para seguir con la feature siguiente.
* En caso de tener que regresar a rehacer otra feature en etapas avanzadas del desarrollo, se dividirá el equipo en pruebas y desarrollo para reparar todo lo más rápido posible.
* En caso de un problema que retrase el desarrollo, se dejarán features para una versión posterior y se ajustará el MVP
* Se debe mantener un buen ritmo de trabajo para asegurar la entrega de la primera versión el 25 de noviembre de 2022 y evitar sobrecarga de trabajo

## 18. Personas que pueden aprobar las pruebas
Para poder pasar a la siguiente parte del desarrollo, necesitamos la aprobación de alguno de nuestros clientes:
* Paulina Bustos
* Arturo Fernández
