# Práctica 3. Android Studio: configuración y perfiles de dispositivos virtuales (AVD)

**Módulo:** Programación Multimedia y Dispositivos Móviles  
**Curso:** 2.º DAM  
**Modalidad:** Individual  
**Calificación:** 10 puntos  
**Resultado de aprendizaje:** **RA1.** Aplica tecnologías de desarrollo para dispositivos móviles evaluando sus características y capacidades.

---

## 1. Criterios de evaluación

Esta práctica obtiene evidencias principalmente de los siguientes criterios de evaluación:

- **RA1.d)** Se han identificado configuraciones que clasifican los dispositivos móviles en base a sus características.
- **RA1.e)** Se han descrito perfiles que establecen la relación entre el dispositivo y la aplicación.
- **RA1.h)** Se han utilizado emuladores para comprobar el funcionamiento de las aplicaciones.

La creación y configuración de los AVD permite trabajar especialmente los criterios **d** y **e**. La ejecución de una aplicación y las operaciones realizadas sobre el emulador aportan evidencia del criterio **h**.

---

## 2. Objetivos de la práctica

Al finalizar la práctica el alumno deberá ser capaz de:

- Identificar los principales tipos de dispositivos que puede simular Android Emulator.
- Diferenciar **perfil de hardware**, **imagen del sistema** y **AVD**.
- Crear dispositivos virtuales a partir de perfiles predefinidos.
- Crear un **perfil de hardware personalizado** a partir de las características de un dispositivo real.
- Seleccionar una imagen del sistema y relacionarla con su versión de Android y nivel de API.
- Configurar orientación, memoria y almacenamiento de un AVD.
- Ejecutar una aplicación Android en un dispositivo virtual.
- Localizar la aplicación instalada mediante **Device Explorer**.
- Restablecer los datos de un AVD mediante **Wipe Data**.
- Documentar y justificar las configuraciones realizadas.

---

## 3. Parte 1. Tipos de dispositivos que puede emular Android Studio — 1 punto

Accede a:

**View → Tool Windows → Device Manager → + → Create Virtual Device**

En la ventana **Select Hardware**, identifica los tipos de dispositivos que permite configurar tu versión de Android Studio.

Realiza una tabla como la siguiente:

| Tipo de dispositivo | ¿Para qué se utiliza? | Ejemplo de perfil disponible en tu Android Studio |
|---|---|---|
| Phone/Tablet | | |
| Wear OS | | |
| Android TV / Google TV | | |
| ChromeOS Device | | |
| Android Automotive | | |

> **Importante:** los perfiles disponibles pueden variar según la versión de Android Studio. Debes indicar ejemplos que aparezcan realmente en la instalación utilizada en el aula.

Incluye **una captura de Select Hardware** donde se observen las categorías disponibles.

---

## 4. Parte 2. Creación de tres dispositivos virtuales — 6 puntos

Debes configurar **tres AVD diferentes**.

### 4.1. AVD 1 — Tablet Nexus 10 — 1,5 puntos

Crea un dispositivo virtual con estas condiciones:

- **Perfil de hardware:** Nexus 10.
- **Sistema:** Android 15 **Vanilla Ice Cream**.
- **API:** 35.
- **Orientación inicial:** Landscape (horizontal).

Si el perfil Nexus 10 no aparece directamente en tu versión de Android Studio, utiliza un perfil de tablet equivalente o crea/clona un perfil que reproduzca sus características e indica claramente qué solución has utilizado.

Completa la siguiente ficha:

| Característica | Configuración realizada |
|---|---|
| Nombre del AVD | |
| Perfil de hardware | |
| Imagen del sistema / Android | |
| Nivel de API | |
| Arquitectura de la imagen | |
| Tamaño de pantalla | |
| Resolución | |
| Densidad | |
| Orientación inicial | |
| Cámaras | |
| Memoria RAM | |
| Almacenamiento interno | |
| Tarjeta SD / almacenamiento externo | |

**Evidencias:** captura de la configuración final del AVD y captura del emulador iniciado en orientación horizontal.

### 4.2. AVD 2 — Pixel 8 — 1,5 puntos

Crea un segundo AVD con estas condiciones:

- **Perfil:** Pixel 8.
- **Sistema:** Android 14.
- **API:** 34.
- **Orientación inicial:** Portrait (vertical).

Completa la misma ficha de características utilizada para el AVD anterior.

**Evidencias:** captura de la configuración final y captura del Pixel 8 ejecutándose en orientación vertical.

### 4.3. AVD 3 — Perfil personalizado basado en OnePlus 12 — 3 puntos

Android Studio no proporciona necesariamente un perfil predefinido para el OnePlus 12. Por ello, debes **investigar sus especificaciones y crear un perfil de hardware personalizado**.

Ruta orientativa:

**Device Manager → + → Create Virtual Device → New Hardware Profile**

Investiga las especificaciones del **OnePlus 12** utilizando preferentemente la web oficial del fabricante.

Como referencia, el modelo comercial dispone, según versión, de características como:

- Pantalla: **6,82 pulgadas**.
- Resolución: **3168 × 1440 píxeles (QHD+)**.
- Densidad aproximada: **510 ppp**.
- Sistema de lanzamiento: **OxygenOS 14 basado en Android 14**.
- RAM comercial: **12 GB o 16 GB**.
- Almacenamiento comercial: **256 GB o 512 GB**.
- Cámara frontal y cámaras traseras.

Debes distinguir entre las **especificaciones del teléfono físico** y lo que Android Emulator permite reproducir. No se pretende simular exactamente su procesador Snapdragon, GPU, rendimiento fotográfico, batería o velocidad real del dispositivo.

#### Trabajo que debes realizar

1. Busca las especificaciones del OnePlus 12.
2. Cita la fuente utilizada.
3. Crea un nuevo perfil llamado, por ejemplo, **OnePlus 12 - Alumno**.
4. Introduce las características que puedan trasladarse razonablemente al perfil de hardware.
5. Crea un AVD utilizando ese perfil y una imagen **Android 14 / API 34**.
6. Inicia el emulador y comprueba que funciona.

Completa dos tablas.

**A. Investigación del dispositivo real**

| Característica | OnePlus 12 real | Fuente |
|---|---|---|
| Tamaño de pantalla | | |
| Resolución | | |
| Densidad | | |
| RAM | | |
| Almacenamiento | | |
| Versión Android de referencia | | |
| Cámara frontal | | |
| Cámaras traseras | | |

**B. Perfil creado en Android Studio**

| Característica | Valor configurado en el AVD |
|---|---|
| Nombre | |
| Imagen del sistema / API | |
| Tamaño | |
| Resolución | |
| Densidad | |
| Orientación inicial | |
| Cámaras | |
| Memoria RAM | |
| Almacenamiento interno | |
| Tarjeta SD / almacenamiento externo | |

Finalmente responde:

**¿Qué características del OnePlus 12 real no pueden reproducirse fielmente mediante un AVD? Explica al menos tres.**

**Evidencias:** captura de **Configure Hardware Profile**, captura de la configuración final del AVD y captura del emulador en funcionamiento.

---

## 5. Parte 3. Uso del emulador — 2 puntos

Utiliza el **AVD Nexus 10** creado anteriormente.

### 5.1. Ejecutar una aplicación — 0,75 puntos

a) Abre un proyecto Android sencillo realizado en clase o crea uno de prueba.  
b) Selecciona el AVD Nexus 10 como dispositivo de ejecución.  
c) Ejecuta la aplicación.  
d) Comprueba que aparece correctamente en el emulador.  
e) Incluye una captura donde se vea la aplicación ejecutándose.

### 5.2. Localizar la aplicación instalada — 0,75 puntos

Utiliza **Device Explorer** para localizar los archivos asociados a la aplicación instalada.

Indica:

a) El **package name** de la aplicación.  
b) La ruta que has localizado.  
c) Qué contiene esa ubicación.  
d) Si puedes acceder o no a todos los directorios y por qué.  
e) Incluye una captura del explorador donde se identifique la aplicación.

> No es suficiente escribir una ruta obtenida de Internet: debe corresponder al proyecto que has ejecutado.

### 5.3. Restablecer el AVD — 0,5 puntos

a) Cierra el emulador.  
b) Abre **Device Manager**.  
c) En el menú del AVD Nexus 10 utiliza **Wipe Data**.  
d) Vuelve a iniciar el AVD.  
e) Comprueba que los datos y aplicaciones instaladas por el usuario han sido eliminados.  
f) Incluye una captura antes o después del proceso y explica brevemente qué hace **Wipe Data**.

---

## 6. Preguntas de reflexión

Responde brevemente:

a) ¿Qué diferencia existe entre un **perfil de hardware** y un **AVD**?  
b) ¿Qué diferencia existe entre el perfil Pixel 8 y la imagen Android 14/API 34 que has utilizado?  
c) ¿Por qué dos AVD pueden utilizar el mismo perfil de hardware pero diferentes versiones de Android?  
d) ¿Un AVD reproduce exactamente el rendimiento de un teléfono físico? Justifica la respuesta.  
e) ¿Para qué puede ser útil probar una misma aplicación en una tablet y en un smartphone?  
f) ¿Qué relación existe entre las características de un dispositivo y los requisitos de una aplicación?

---

## 7. Qué debe entregar el alumno

La entrega constará de **un único informe en PDF**:

**`Practica3_AVD_Apellidos_Nombre.pdf`**

El informe deberá seguir el orden de los ejercicios anteriores. Cada apartado de la entrega debe permitir identificar claramente a qué ejercicio corresponde.

### 7.1. Portada e índice

a) Portada con título de la práctica, nombre y apellidos, curso, módulo y fecha.  
b) Índice del documento.

### 7.2. Correspondencia con el ejercicio 3 — Tipos de dispositivos

a) Tabla de tipos de dispositivos que permite configurar Android Studio.  
b) Explicación breve de para qué se utiliza cada tipo.  
c) Ejemplo de un perfil disponible para cada tipo.  
d) Captura de **Select Hardware** donde se observen las categorías disponibles.

### 7.3. Correspondencia con el ejercicio 4.1 — AVD Nexus 10

a) Tabla completa con las características configuradas.  
b) Captura de la configuración final del AVD.  
c) Captura del emulador iniciado con orientación horizontal.  
d) Explicación de cualquier adaptación realizada si Nexus 10 no aparece como perfil predefinido.

### 7.4. Correspondencia con el ejercicio 4.2 — AVD Pixel 8

a) Tabla completa con las características configuradas.  
b) Captura de la configuración final del AVD.  
c) Captura del emulador Pixel 8 ejecutándose con orientación vertical.

### 7.5. Correspondencia con el ejercicio 4.3 — Perfil personalizado OnePlus 12

a) Tabla de investigación del dispositivo real.  
b) Fuente o fuentes utilizadas para obtener las especificaciones.  
c) Tabla del perfil creado en Android Studio.  
d) Captura de **Configure Hardware Profile**.  
e) Captura de la configuración final del AVD.  
f) Captura del emulador en funcionamiento.  
g) Respuesta sobre, al menos, tres características del OnePlus 12 real que no puedan reproducirse fielmente mediante el AVD.

### 7.6. Correspondencia con el ejercicio 5.1 — Ejecución de la aplicación

a) Captura de la aplicación ejecutándose en el AVD Nexus 10.  
b) Breve explicación del proyecto utilizado y del resultado obtenido.

### 7.7. Correspondencia con el ejercicio 5.2 — Device Explorer

a) **Package name** de la aplicación.  
b) Ruta localizada mediante **Device Explorer**.  
c) Explicación de qué contiene esa ubicación.  
d) Explicación sobre el acceso a los directorios.  
e) Captura de Device Explorer donde pueda identificarse la aplicación.

### 7.8. Correspondencia con el ejercicio 5.3 — Wipe Data

a) Evidencia del proceso de restablecimiento del AVD.  
b) Explicación breve de qué hace **Wipe Data**.  
c) Comprobación de que los datos y aplicaciones instalados por el usuario han sido eliminados.

### 7.9. Correspondencia con el ejercicio 6 — Preguntas de reflexión

a) Respuesta a la pregunta 6.a.  
b) Respuesta a la pregunta 6.b.  
c) Respuesta a la pregunta 6.c.  
d) Respuesta a la pregunta 6.d.  
e) Respuesta a la pregunta 6.e.  
f) Respuesta a la pregunta 6.f.

### 7.10. Conclusiones y webgrafía

a) Conclusión de entre **5 y 10 líneas** sobre lo aprendido durante la práctica.  
b) Webgrafía con las páginas consultadas, URL y fecha de consulta.

### Requisitos de las capturas

a) Deben ser **capturas propias**.  
b) Deben ser legibles.  
c) Cada captura debe llevar un pequeño texto indicando qué demuestra.  
d) Deben permitir identificar claramente la configuración o acción realizada.  
e) No es necesario entregar las carpetas de los AVD ni las imágenes del sistema.

---

## 8. Rúbrica de evaluación

| Indicador evaluado | Criterio | Excelente | Adecuado | Básico | Insuficiente | Máximo |
|---|---|---|---|---|---|---:|
| Identificación de tipos de dispositivos | RA1.d | Identifica correctamente las categorías disponibles, explica su finalidad y aporta ejemplos reales de perfiles. | Identifica las categorías principales y aporta ejemplos con alguna omisión menor. | Identificación parcial o explicaciones muy breves. | No distingue los tipos de dispositivos o aporta información incorrecta. | **1,0** |
| Nexus 10 / Android 15 API 35 | RA1.d | Configuración completa, correcta y documentada; orientación horizontal y evidencias claras. | Configuración correcta con alguna omisión menor en datos o evidencias. | AVD creado pero con errores de configuración o documentación incompleta. | No crea o no acredita el AVD solicitado. | **1,5** |
| Pixel 8 / Android 14 API 34 | RA1.d | Configuración completa, correcta y documentada; orientación vertical y evidencias claras. | Configuración correcta con alguna omisión menor. | AVD creado pero con errores o documentación incompleta. | No crea o no acredita el AVD solicitado. | **1,5** |
| Perfil personalizado OnePlus 12 | RA1.d / RA1.e | Investiga fuentes fiables, crea un perfil coherente, diferencia dispositivo real y virtual y justifica limitaciones. | Perfil correctamente creado y documentado, con pequeñas omisiones. | Perfil parcialmente ajustado al modelo real o investigación/justificación insuficiente. | No crea el perfil personalizado o los datos carecen de fundamento. | **3,0** |
| Ejecución de la aplicación | RA1.h | Ejecuta correctamente la app en el AVD y aporta evidencia clara. | Ejecución correcta con evidencia poco explicada. | Evidencia incompleta o necesita ayuda importante. | No demuestra la ejecución. | **0,75** |
| Device Explorer y localización | RA1.h | Localiza la app, identifica package name y ruta y explica correctamente lo observado. | Localiza la aplicación con alguna explicación incompleta. | Presenta evidencia parcial o confunde ruta/package. | No localiza la aplicación. | **0,75** |
| Wipe Data | RA1.h | Realiza el restablecimiento y explica correctamente su efecto con evidencia. | Realiza el proceso con explicación breve. | Evidencia incompleta o explicación confusa. | No realiza o no acredita el proceso. | **0,5** |
| Presentación, reflexión y webgrafía | RA1.e | Informe completo, ordenado, con portada, índice, conclusiones, respuestas razonadas y fuentes correctamente identificadas. | Informe completo con pequeñas carencias formales. | Faltan varios elementos o las respuestas son poco razonadas. | Entrega desorganizada, sin fuentes o con apartados esenciales ausentes. | **1,0** |
| **TOTAL** | | | | | | **10,0** |

### Cálculo de la rúbrica

Para cada indicador se aplicará:

- **Excelente:** 100 % de la puntuación.
- **Adecuado:** 75 %.
- **Básico:** 50 %.
- **Insuficiente:** 0 %.

La nota final será la suma de las puntuaciones obtenidas en todos los indicadores.

---

## 9. Fuentes recomendadas

Utiliza preferentemente documentación oficial:

- Android Developers — Crear y administrar dispositivos virtuales:  
  https://developer.android.com/studio/run/managing-avds
- Android Developers — Android Emulator:  
  https://developer.android.com/studio/run/emulator
- Android Developers — Versiones y niveles de API de Android:  
  https://developer.android.com/guide/topics/manifest/uses-sdk-element
- OnePlus — Especificaciones oficiales del OnePlus 12:  
  https://www.oneplus.com/es/12/specs

> Las interfaces y perfiles disponibles pueden cambiar entre versiones de Android Studio. Si alguna opción indicada en el enunciado no aparece exactamente con ese nombre, documenta la alternativa utilizada y justifica la decisión.
