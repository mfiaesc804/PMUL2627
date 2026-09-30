# Práctica 3. Android Studio, configuraciones y perfiles de dispositivos virtuales

**Módulo:** Programación Multimedia y Dispositivos Móviles  
**Curso:** 2.º DAM  
**Tipo:** Individual, con comprobación práctica en el aula  
**Resultado de aprendizaje:** RA1. Aplica tecnologías de desarrollo para dispositivos móviles evaluando sus características y capacidades.

## 1. Criterios de evaluación

Esta práctica recoge evidencias de los siguientes criterios de RA1:

- **c)** Instalación, configuración y utilización de entornos de trabajo para desarrollo móvil.
- **d)** Identificación de configuraciones que clasifican dispositivos según sus características.
- **e)** Descripción de perfiles que relacionan el dispositivo con los requisitos de una aplicación.
- **h)** Utilización de emuladores para comprobar el funcionamiento de aplicaciones.

Los enunciados anteriores son resúmenes operativos de los criterios. La ejecución en emulador se profundizará en la práctica 4.

## 2. Objetivos

- Preparar Android Studio y las herramientas necesarias para trabajar.
- Distinguir IDE, SDK, imagen de sistema, perfil de hardware y AVD.
- Clasificar dispositivos utilizando características comprobables.
- Relacionar una configuración de dispositivo con las necesidades de una app.
- Crear y ejecutar un proyecto de prueba en dos configuraciones virtuales.
- Registrar las pruebas y diagnosticar una incidencia real o un caso de incompatibilidad razonado.

## 3. Situación de partida

El departamento va a probar una aplicación de consulta de rutas en teléfonos y tabletas. Antes de desarrollar sus funcionalidades, debes preparar el entorno y justificar qué dispositivos virtuales utilizarías.

Trabajarás con un proyecto sencillo llamado **RutasRA1**. En esta práctica solo se ejecutará la pantalla inicial que genera Android Studio; no se pide desarrollar todavía un planificador de rutas.

### Recursos

- Ordenador con conexión a Internet y espacio suficiente para Android Studio, SDK e imágenes de sistema.
- Permisos de instalación o un equipo del aula preparado por el centro.
- Documentación oficial de Android.

Comprueba los requisitos actuales en la documentación, sin asumir que son iguales para ejecutar solo el IDE y para ejecutar también el emulador. Si el ordenador no permite emulación, acuerda con el profesor el uso de otro equipo del aula. Un informe teórico o una prueba solo en un teléfono físico no sustituye la evidencia del criterio h).

## 4. Instalación y configuración del entorno — RA1.c

1. Comprueba el sistema operativo, la RAM, el espacio libre y la disponibilidad de aceleración o virtualización del equipo.
2. Instala una versión estable de Android Studio desde su página oficial. Si está preinstalado, documenta su versión y completa una instalación o actualización de un componente del SDK supervisada por el profesor.
3. Localiza el SDK Manager e identifica la ruta del SDK.
4. Instala una plataforma Android, Platform Tools, Android Emulator y las imágenes necesarias para los AVD que configurarás.
5. Comprueba el JDK utilizado por Gradle; utiliza la configuración compatible recomendada por el IDE. No cambies versiones de Java o Gradle al azar.
6. Crea el proyecto **RutasRA1**, con paquete **com.tunombre.rutasra1**, lenguaje **Kotlin** y una plantilla de actividad vacía con **Views/XML**, normalmente denominada **Empty Views Activity**.
7. Utiliza **minSdk 24** si las herramientas elegidas lo admiten; si el centro utiliza otro mínimo, registra el valor acordado. Mantén los valores de `compileSdk` y `targetSdk` compatibles con la plantilla y anótalos.
8. Espera a la sincronización, compila y localiza el manifiesto, la actividad principal y su layout.

**Evidencias:** versión del IDE; componentes instalados; configuración del proyecto; compilación correcta. Añade una explicación breve de la diferencia entre `minSdk`, `compileSdk` y `targetSdk`.

**Pregunta:** ¿instalar una plataforma nueva en el SDK actualiza Android en un teléfono físico? Justifica la respuesta.

## 5. Clasificación de configuraciones — RA1.d

Antes de crear los AVD, compara **tres configuraciones**. Dos se implementarán como AVD y la tercera puede ser una configuración candidata que finalmente descartes.

| Característica | Configuración A | Configuración B | Configuración C |
|---|---|---|---|
| Tipo: teléfono, tableta u otro | | | |
| Perfil/modelo utilizado como referencia | | | |
| Tamaño de pantalla y resolución | | | |
| Densidad y orientación | | | |
| Memoria RAM configurada | | | |
| Almacenamiento configurado | | | |
| Versión de Android y nivel de API | | | |
| Arquitectura de la imagen: x86_64, arm64 u otra | | | |
| Sensores/capacidades disponibles o simulados | | | |
| Tipo de imagen y servicios incluidos | | | |
| Clasificación y uso que propones | | | |

Explica qué características permiten clasificarlas y qué diferencias pueden afectar a una aplicación. No basta con copiar tres nombres comerciales.

Distingue los datos del perfil virtual de las especificaciones de un dispositivo físico. No atribuyas al AVD el rendimiento real del modelo que representa.

## 6. Perfiles de aplicación y compatibilidad — RA1.e

En esta actividad se emplea **perfil de uso de la aplicación** como una ficha de requisitos para relacionar app y dispositivo. No es lo mismo que el **perfil de hardware del AVD**, que describe el dispositivo virtual.

Elabora una ficha para cada caso:

- **Perfil A — Consulta de rutas:** muestra fichas de rutas, permite elegir manualmente origen y destino y debe poder usarse en teléfono y tableta. No necesita conocer la ubicación actual.
- **Perfil B — Seguimiento de una ruta:** además de consultar información, necesita recibir la ubicación durante el uso y presentar el progreso. Debe informar cuando no obtiene ubicación o no dispone del permiso necesario.

Para cada ficha:

1. Distingue requisitos **obligatorios** y capacidades **opcionales**.
2. Relaciónalos con la pantalla, versión/API, memoria, almacenamiento y capacidades del dispositivo. Cuando un requisito no tenga un mínimo numérico dado, formula una hipótesis de prueba y justifícala; no inventes un requisito oficial.
3. Evalúa la compatibilidad con las tres configuraciones del apartado anterior.
4. Indica si cada combinación es **compatible**, **compatible con condiciones** o **no compatible**, y explica por qué.
5. Propón una alternativa cuando falte una capacidad y señala qué función se perdería.

| Perfil de la app | Configuración | Resultado de compatibilidad | Justificación | Alternativa o prueba necesaria |
|---|---|---|---|---|
| A | A | | | |
| A | B | | | |
| A | C | | | |
| B | A | | | |
| B | B | | | |
| B | C | | | |

Este apartado es un análisis de requisitos: **no tienes que programar ubicación ni solicitar permisos** en esta práctica. Tampoco debes presentar la hipótesis de compatibilidad como una funcionalidad ya comprobada.

## 7. Creación y uso de AVD — RA1.c y RA1.h

1. Crea dos AVD en Device Manager: **un teléfono y una tableta**.
2. Utiliza **dos niveles de API distintos**, ambos iguales o superiores al `minSdk` del proyecto. Elige imágenes disponibles y compatibles con el ordenador del aula.
3. Registra el perfil de hardware, la imagen de sistema y las propiedades de cada AVD. Distingue una imagen AOSP de una con Google APIs o Google Play, cuando esas opciones estén disponibles.
4. Inicia cada emulador y comprueba que llega a la pantalla de inicio.
5. Ejecuta **RutasRA1** en ambos, de uno en uno si los recursos del ordenador son limitados.
6. En cada AVD, comprueba la apertura desde el lanzador, el cambio de orientación y la salida a Inicio con posterior retorno a la app.
7. Localiza el proceso de la app en Logcat e identifica el emulador al que está conectado el IDE.

Registra el resultado real: no es suficiente que el AVD aparezca en la lista de dispositivos.

| Prueba | AVD/API | Pasos | Resultado esperado | Resultado observado | Evidencia |
|---|---|---|---|---|---|
| Instalación y primera ejecución | | | | | |
| Apertura desde el lanzador | | | | | |
| Cambio de orientación | | | | | |
| Inicio y retorno | | | | | |

Repite las cuatro pruebas en cada AVD.

## 8. Diagnóstico y conclusiones

Describe una incidencia real indicando síntoma, comprobaciones, causa probable, actuación y resultado. Si no se produce ninguna, analiza este caso sin necesidad de instalar otra imagen:

> El proyecto tiene `minSdk 28` y se intenta ejecutar en un AVD con API 26.

Explica la incompatibilidad y propón alternativas razonadas. No reduzcas `minSdk` sin comprobar si el código y las dependencias admiten ese cambio.

Concluye respondiendo:

- ¿Por qué elegiste esas dos configuraciones?
- ¿Qué diferencia hay entre un perfil de hardware y un perfil de requisitos de la app?
- ¿Qué has comprobado realmente y qué requeriría una app completa o un dispositivo físico?

## 9. Entrega

Entrega:

1. **`Practica3_NombreApellidos.pdf`**, con 5–8 páginas orientativas: entorno, comparación de configuraciones, perfiles de aplicación, AVD, pruebas, diagnóstico y fuentes.
2. **`Practica3_NombreApellidos.zip`**, con el proyecto RutasRA1.

Incluye en el proyecto los archivos fuente, recursos, manifiesto, scripts de construcción y Gradle Wrapper. Excluye `local.properties`, carpetas `build/`, `.gradle/`, imágenes del emulador, SDK y credenciales. No entregues los AVD completos: documenta su configuración en el informe.

Las capturas deben mostrar las evidencias necesarias y llevar una explicación. El profesor podrá solicitar una demostración de ejecución y que localices la configuración del proyecto.

## 10. Rúbrica de evaluación

| Indicador | Criterio | Excelente — 100 % | Adecuado — 75 % | Básico — 50 % | Insuficiente — 0 % | Máximo |
|---|---|---|---|---|---|---:|
| Instalación, configuración y uso del entorno | c | Acredita instalación o intervención supervisada, configura SDK/proyecto y compila; explica la función de los componentes y las versiones. | Entorno operativo y evidencias suficientes, con alguna explicación incompleta. | Configuración parcialmente acreditada o uso con ayuda frecuente; distingue solo parte de los componentes. | No acredita un entorno utilizable ni su configuración. | 3 |
| Clasificación de dispositivos | d | Compara tres configuraciones con datos verificables y explica su clasificación y consecuencias para las apps. | Compara las tres con alguna omisión menor y una clasificación razonada. | Comparación parcial o clasificación poco justificada. | Solo enumera modelos o presenta datos esenciales incorrectos. | 2 |
| Perfiles y relación dispositivo–aplicación | e | Define los dos perfiles, distingue requisitos y opcionales y justifica las seis combinaciones de compatibilidad y alternativas. | Describe los dos perfiles y la mayoría de las relaciones correctamente. | Confunde algunos requisitos o ofrece relaciones genéricas sin suficiente justificación. | No relaciona requisitos de la aplicación y capacidades de los dispositivos. | 2 |
| Comprobación de la app en emuladores | h | Ejecuta la app en ambos AVD y documenta las ocho pruebas con resultados reales y evidencias identificables. | Ejecuta en ambos y acredita la mayoría de las pruebas, con omisiones menores. | Solo acredita ejecución y pruebas parciales en un AVD. | No demuestra ejecución de la aplicación en un emulador. | 3 |
| **TOTAL** | | | | | | **10** |

**Cálculo:** peso máximo × coeficiente del nivel (1; 0,75; 0,50; 0). Suma las puntuaciones y redondea la nota final a dos decimales.

Las capturas, explicaciones y demostraciones son evidencias de cada indicador, no criterios independientes. Se valorará el diagnóstico razonado; una incidencia del equipo documentada no debe confundirse con desconocimiento, pero exige una comprobación posterior para acreditar la ejecución.

## 11. Fuentes

Consulta páginas concretas y registra la fecha de consulta:

- [Instalar Android Studio](https://developer.android.com/studio/install).
- [Crear y gestionar AVD](https://developer.android.com/studio/run/managing-avds).
- [Ejecutar apps en Android Emulator](https://developer.android.com/studio/run/emulator).
- [Configurar la construcción de una app](https://developer.android.com/build).
- [Referencia estatal de RA1: Real Decreto 405/2023](https://www.boe.es/eli/es/rd/2023/05/29/405).

