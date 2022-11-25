# Kanik

---

Repositorio que contiene la aplicación Kanik, el software para organizar asesorías entre estudiantes del ITAM.

**Equipo:** Enchiladas Rojas

**Integrantes:**
- Yohaly Lorena Mondragón Sandoval
- Armando Limón Bautista
- Mauricio de Ariño Bello
- Erick Martínez Hernández

# Software Requirements

---

- **Versión:** 1.0
- **Fecha de actualización:** Noviembre 2022

## 1. Introducción

### 1.1 Propósito

El propósito de este documento es exponer el proceso de construcción del software **Kanik** que consiste en una aplicación que permite a los estudiantes de la Comunidad ITAM organizar asesorías de todas las materias curriculares del ITAM. **Kanik** busca centralizar y formalizar la manera en que los alumnos puedan solicitar apoyo a otros alumnos para la resolución de tareas, ejercicios, prácticas, etc. Asímismo, la plataforma busca reunir todo el material posible para complementar los estudios de cada asignatura que los estudiantes del ITAM tengan en sus respectivas carreras.

### 1.2 Convenciones del documento

|Concepto|Definición|
|--|--|
|JS|JavaScript|
|BD|Base de Datos|

### 1.3 Sugerencias de lectura

El documento que se está presentando forma parte de la documentación oficial de la aplicación **Kanik** y está dirigido, especialmente, a toda aquella persona de la Comunidad ITAM que esté interesada en realizar sus contribuciones al proyecto.

### 1.4 Alcance del producto

Actualmente no existe una herramienta respaldada oficialmente por el ITAM la cual tome como enfoque las relaciones entre estudiantes al servir como plataforma para sus necesidades académicas. **Kanik** busca acomodar esta carencia fomentando el estudio entre estudiantes que están por terminar sus carreras y aquellos recién inician con el objetivo de facilitar el entendimiento de las asignaturas, así como proveer el material necesario para las mismas.

### 1.5 Referencias

- **Repositorio de GitHub**: https://github.com/ArmandoLimn/Kanik-Asesorias-ITAM

## 2. Descripción General

### 2.1 Perspectiva del producto

La aplicación **Kanik** es distinta de otras aplicaciones ya que se enfoca en el alumnado del ITAM, por lo que, el público objetivo es bien conocido y se sabé una gran parte de las necesidades de estudio.

### 2.2 Funciones del producto

La aplicación **Kanik** debe cumplir con las siguientes funcionalidades:

- Los usuarios deben poder vincular su cuenta del ITAM, iniciar y cerrar sesión.
- Los tutores deben poder registrar, modificar y cancelar sus asesorías (horario, materias, costo).
- Los estudiantes deben poder aceptar, cancelar o proponer un nuevo horario para las asesorías.
- Los estudiantes pueden realizar una búsqueda de asesorías mediante filtros (tutor, asignatura, costo, etc.)

### 2.3 Clases de usuario y características

- **Tutores:**
    - Son los estudiantes que ofrecen e imparten las asesorías.
    - Pueden cobrar o no por sus asesorías.
    - Pueden registrar todas las asesorías que sean necesarias.
- **Estudiantes:**
    - Son los estudiantes que solicitan las asesorías.
    - Pueden proponer un nuevo horario para la asesoría.
    - Pueden cancelar su asesoría.

### 2.4 Ambiente Operativo

**Kanik** utiliza una gran variedad de herramientas para su buen funcionamiento, a continuación, se detallan las más importantes:

- **JS:** es el lenguaje de programación de alto nivel utilizado en el desarrollo.
- **Angular:** framework basado en JS para el front de la aplicación.
- **Git/GitHub:** herramienta de control de versiones y su respectivo almacenamiento en la nube.

### 2.5 Restricciones de Diseño e Implementación

**Kanik** se encuentra aún en fase de desarrollo, por lo que muchas de las funcionalidades son meramente simuladas por la aplicación. Ejemplo de ello, son el registro de las asesorías, pues aunque funcionan todos los elementos de la aplicación, aún no se almacena la infromación en una base de datos.

### 2.6 Supuestos

A continuación, se asumió lo siguiente:
- El ITAM nos permitió vincular las credenciales de los estudiantes a nuestra aplicación.
- La aplicación funciona solamente con estudiantes activos, no se toma en cuenta a exalumnes.
- El ITAM nos proporcionó una vista de las BD para consultar las asignaturas que se están impartiendo en el semestre en curso.
- Las Bases de Datos de **Kanik** están en funcionamiento.

## 3. Requerimientos de la Interfaz de Usuario

## 4. Características del Sistema

### 4.1 Inicio de Sesión

- **Descripción:** interfaz que permite registrar las credenciales del ITAm para vincular y/o acceder a la plataforma.
- **Usuarios:** tutores y estudiantes.
- **Prioridad**: alta.
- **Requerimientos funcionales:**
    1. El usuario ingresará sus credenciales y, si son correctas, podrá acceder a la aplicación.
    2. Si son erróneas mostrará un mensaje de error.
    3. Si en el registro ya está registrado el correo se le notificará al usuario.

### 4.2 Registro, Modificación y Cancelación de Asesorías

- **Descripción:** interfaz que permite dar de alta una asesoría, modificarla y, si fuese necesario, eliminarla/cancelarla.
- **Usuarios:** tutores.
- **Prioridad:** alta.
- **Requerimientos funcionales:**
    1. El tutor puede configurar la asignatura que impartirá, los posibles horarios y, si es el caso, el costo por ese horario.
    2. Para comodidad del tutor se podrá modificar cualquiera de los campos ya mencionados.

### 4.3 Aceptar y Cancelar Asesoría y Propuesta de Asesoría
- **Descripción:** interfaz que permite a los estudiantes realizar cualquier modificación a una asesoría aceptada o por aceptar.
- **Usuarios:** estudiantes.
- **Prioridad:** alta.
- **Requerimientos funcionales:**
    1. El estudiante puede aceptar un horario ya definido por el tutor.
    2. El estudiante puede proponer un nuevo horario para la asesoría.
    3. El estudiante puede cancelar la asesoría.

## 5. Requerimientos No Funcionales

### 5.1 Requerimientos de Rendimiento

- Sistema Windows 7 o superior.
- Navegador con base Chromium 102 o superior.
- Conexión estable de internet.

### 5.2 Requerimientos de Seguridad

- Para asegurar la privacidad de los datos se recomienda el uso de una conexión o red privada.
- Se sugiere no guardar la contraseña en las opciones por defecto del navegador.
- Solamente se podrá usar el correo institucional del ITAM para crear la cuenta y usar la aplicación.

### 5.3 Calidad de Software

**Kanik** es una plataforma que se adapta a las crecientes necesidades de los estudiantes de la Comunidad ITAM, pues constantemente se están agregando material adicional a los cursos como ejercicios de práctica, lecturas, etc., que ayuden a los estudiantes en su proceso de aprendizaje de cada una de las materias en las que requieran ayuda.

# Plan de Calidad

---


# Arquitectura

---

La aplicación **Kanik** utiliza una pequeña variación de la arquitectura por microservicios. Por un lado, **Kanik** busca crecer y cada vez más estudiantes tengan acceso a estas herramientas y materiales adicionales que son de gran ayuda. Por el otro, requerimos de un desarrollo rápido y eficiente, así como de una tanda de pruebas rápidas.

Asimismo, como cada servicio es independiente uno del otro, es mucho más sencillo administrarlo, pues si encontramos algún error es fácil encontrarlo y solucionarlo.

Por otra parte, incluye un fragmento de arquitectura API REST ya que requerimos de algunas funcionalidades que nos ofrece Google, sobre todo, al momento de agendar, reprogramar o cancelar una asesoría.

# Metodología

---

Durante el desarrollo de **Kanik** se implementó una metodología conocida como **en Cascada** que es una de las más populares en la industria por su simplicidad pero también por su utilidad. Este modelo permite enfocarnos en cada uno de los requerimientos y así asegurar que cada uno se haya desarrollado adecuadamente. La metodología no permite continuar con una fase posterior hasta que se haya concluido la que esté en curso.

La metodología funciona siempre y cuando se tenga una planeación muy profunda, consciente y efectiva, ya que no podemos cometer ningún error ni de planeación ni de codificación, pues esto retrasaría la fase en la que nos encontremos y, en general, todo el proyecto.

Finalmente, como conocemos el alcance que puede llegar a tener la aplicación y tenemos claros los requerimientos (funcionales y no funcionales) la metodología de **en Cascada** es la más adecuada al proyecto.

# Código

---

# Propuesta económica

---

`Última actualización: noviembre 2022`
