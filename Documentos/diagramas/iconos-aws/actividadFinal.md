# Ejercicio práctico Asistente de soporte Documental

Nombre de proyecto: **PARES · Arquitectura RAG en AWS**
Alumno: German Dario Realpe Zambrano. Actividad FINAL · Arquitecturas con IA. 
Fecha: 7 de noviembre de 2026.
Universidad: PONTIA
MATERIA: Arquitecturas con IA
Máster en IA, Cloud Computing & DevOps - 0226

## Contexto del proyecto

`PARES` es el (Portal de Archivos Españoles del Ministerio de Cultura) y es la principal plataforma de difusión del Patrimonio Histórico Documental Español, creada y gestionada por la Subdirección General de los Archivos Estatales, del Ministerio de Cultura.

`PARES` Contiene fichas descriptivas e imágenes digitalizadas de los fondos documentales conservados
en los Archivos Estatales, Sin embargo, en `PARES` no figura aun toda la documentación de nuestros archivos, debido al enorme volumen de la misma. 

Los contenidos de `PARES` van aumentando a medida que se desarrollan los trabajos archivísticos de identificación, descripción y digitalización de los documentos.

## Planteamiento del ejercicio

Se requiere diseñar un sistema que permita una consulta en lenguaje natural basado en la base de datos.
Para ello, supondremos que los documentos escaneados estan en algun componente cloud que permita su almacenamiento, con posibilidad de realizar mas ingestas de documentos.

- Los documentos para el ejercicio estaran fechados entre los años 1500 a 1600.
- Las fuentes documentales seran elementos escaneados sin estructuras definidas.
- Se requiere que el tratamiento permita el "entendimiento" del contenido de los documentos.
- Se requiere que se pueda generar una metadata basada en fechas y vinculada a hechos conocidos o que puedan ser identificados basandose en los documentos, permitiendo generar un indice de los mismos con referencias a los documentos escaneados.
- La solucion proveera de un frontal web con buscador inicial que permita explorar los diferentes hechos registrados, el resultado de este buscador, permitirá la obtención de resúmenes de los hechos clasificados según un indice.

- El portal tambien tendra la entrada de lenguaje natural para poder realizar peticiones de resúmenes o datos disponibles,
Un posible prompt del usuario podría ser este Ejemplo :
"Necesito el nombre de las naves españolas que participaron en las jornadas de la
Batalla de San Miguel, indicando los siguientes datos si se dispone de ellos: nombre,
año de construcción, arqueo en toneles, nombre del capitán de mar y del capitán de
guerra, marinería embarcada, si también se encontraba embarcado un tercio, indicar
el nombre del tercio embarcado. Indicar tambien la nave capitana y la almiranta. Por
último, si se desplegó en un grupo de naves, indicar el grupo en el que estaba como
grupo 1, grupo 2, etc. y el nombre del capitán que la comandaba y su nave principal"

- Se podra devolver la informacion tanto en formato texto o en formato pdf para su descarga (si el usuario asi lo solicita).
- El acceso de los usuarios debera ser utilizando un sistema IDP basado en alguna de las credenciales disponibles como el ID de Google, Microsoft u otro.
- Los usuarios podran tener diferentes roles Como:
    - **Administradores**: serán aquellos que podrán hacer funciones como la subida de
        nuevos documentos, acceder a la gestión de usuarios, verificar la calibración de los
        modelos, acceder a las trazas de uso y al apartado de informes de utilización de la
        solución

    - **Usuarios**: seran aquellos que pueden acceder a la solucion tanto al buscador inicial
        como al buscador de lenguaje natural

## Entregables:

Requerimientos del documento a entregar: La estructura utilizada en el documento de arquitectura. Al menos se debe atender a los siguientes apartados:

1. Diagrama y detalle a alto nivel funcional (pudiendose indicar estos como puntos de los requerimientos de la solución).
2. Tipologia de datos, asi como su tratamiento.
3. Integracion de sistemas o soluciones.
4. Diagrama técnico de alto nivel (debera tener los componentes utilizados, Se podran agrupar el uso de funciones en un unico icono).
5. Detalle tecnico que debera atender al detalle de la solución (listando que uso tienen).
6. Seguridad de la solucion, con apartados como autenticacion, autorización, securización de los datos e integraciones con sistemas externos (si se estima oportuno).
7. Registros, logs y trazas (si se estima oportuno).
8. Descripcion de los elementos de control del modelo o modelos empleados (alimentacion de información, calibración, etc.)
9. Monitorizacion funcional y técnica. 
10. Alta disponibilidad y Disaster Recovery (si se estima oportuno)
11. Justificación de la Arquitectura RAG Seleccionada (texto breve).
12. Flujo o diagrama funcional con descripción o breve detalle de los pasos.
13. Diagrama de Arquitectura Cloud (imagen o utilizando herramientas de diagramacion como draw.io, Lucidchart, o incluso Google Sheets)
14. Descripción de Componentes utilizados.
15. Debe quedar claro el flujo de los datos.
16. El documento final [debe quedar en `PARES Arquitectura RAG en AWS` ](https://docs.google.com/document/d/1dp_MKH-TwlOP7IleoKUKnfJo-T_KMMHCHyUAZ1qAexE/edit?usp=sharing)
17. Crea este mismo archivo de entrega en el archivo: ./Documentos/ActividadFinal.md
18. Agrega a estos archivos los diagramas solicitados.
19. A partir de los diagramas creados, genera sus versiones de diagrama técnicos, que cumplan con la normatividad de AWS y azure. he incorpora este capitulo a ActividadFinal.md y `PARES Arquitectura RAG en AWS`


## Estructura del documento 

Para la documentacion de docs de google, si la referencia más adecuada es ISO/IEC/IEEE 42010:2022, porque el documento describirá una arquitectura de software y sus componentes, decisiones y vistas.

### Referencia	Aplicación al documento
- ISO/IEC/IEEE 42010:2022	Organizar la descripción de la arquitectura: interesados, necesidades, vistas, decisiones y relaciones entre ellas. Es la referencia principal. ISO
- ISO/IEC/IEEE 15289:2019	Orientar el propósito y contenido de la documentación técnica de sistemas y software. Complementa la anterior. IEEE

Aplica esta estructura:
1. Portada y control documental: título, autor, organización, fecha, código, versión y estado —por ejemplo, «Propuesta de diseño».
2. Historial de versiones: versión, fecha y descripción del cambio.
3. Índice automático y numeración de páginas.
4. Objetivo, alcance y supuestos.
5. Interesados y necesidades: agentes de Nivel 1, responsables de documentación, ingeniería y seguridad.
6. Requisitos y decisiones de arquitectura: qué debe resolver la solución y por qué se eligieron AWS y sus servicios.
7. Vistas de arquitectura: funcional, componentes, datos, despliegue, red y seguridad; cada figura debe indicar qué explica.
8. Operación y validación: actualizaciones, errores, contexto vacío y criterios de comprobación.
9. Referencias y anexos técnicos.

## Objetivo del Ejercicio a cumplir:

- Agregar una Justificacion de la seleccion de la arquitectura RAG apropiada.
- Agregar descripcion corta y clara de sus componentes abstractos a servicios cloud especificos (AWS o Azure).
- Agregar una descripcion corta y clara del flujo de datos, responsabilidades de los componentes y la justificación de las elecciones tecnológicas. 

## Evaluación del ejercicio
La forma de evaluar el ejercicio sera como se indica a continuación:

- Estructura del dossier 10 pts.
- Diseno de la solucion indicada en el enunciado del ejercicio 30 pts.
- Claridad en los diagramas funcionales / técnicos del dossier 20 pts.
- Claridad de las explicaciones funcionales / técnicas del dossier 30 pts.
- Elementos adicionales de arquitectura que deban ser tenidos en cuenta 10 pts.
- Total 100 pts.

Nota requerida para su aprobado Puntuación 70 pts
Se valorará la claridad del diagrama. Este debe permitir entender de forma correcta la arquitectura presentada.
