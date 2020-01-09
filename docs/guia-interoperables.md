# Guía para la identificación y uso de entidades interoperables

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

## Indice

- [Introducción](#introduccion)
- [Objetivo de esta guía](#objetivo-de-esta-guia)
- [Datos de entidades interoperables](#datos-de-entidades-interoperables)
  - [¿Qué son?](#que-son)
  - [¿Por qué es importante estandarizarlos?](#por-que-es-importante-estandarizarlos)
- [Tipos de entidades interoperables](#tipos-de-entidades-interoperables)
  - [Geográficas](#geograficas)
    - [Países o territorios internacionales](#paises-o-territorios-internacionales)
    - [Divisiones o unidades territoriales internas](#divisiones-o-unidades-territoriales-internas)
      - [A. Comunas -> Barrios -> Fracciones Censales -> Radios Censales (CBFR)](#a-comunas-barrios---fracciones-censales---radios-censales-cbfr)
      - [B. Villas -> Unidades Territoriales de Inclusión Urbana (VUTAI)](#b-villas-unidades-territoriales-de-inclusion-urbana-pm)
      - [C. Otros nomencladores](#c-otros-nomencladores)
      - [D. ¿Cómo nombrar los campos?](#d-como-nombrar-los-campos)
    - [Direcciones y lugares](#direcciones-y-lugares)
    - [**Códigos postales**](#codigos-postales)
  - [**Personas físicas**](#personas-fisicas)
  - [**Perspectiva de Género**](#perspectiva-de-genero)
  - [**Personas jurídicas**](#personas-juridicas)
  - [**Entidades de Gobierno de la Ciudad Autónoma de Buenos Aires**](#entidades-de-gobierno-de-la-ciudad-autonoma-de-buenos-aires)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Introducción

Esta guía busca ayudar a los organismos de la Administración Centralizada y Descentralizada y a las Entidades Autárquicas del Gobierno de la Ciudad Autónoma de Buenos Aires a instrumentar los lineamientos en materia de apertura de datos públicos establecidos en los Decretos N°[156/2012](https://boletinoficial.buenosaires.gob.ar/normativaba/norma/190097) y N° [478/2013](https://boletinoficial.buenosaires.gob.ar/normativaba/norma/234859) y a mejorar la calidad y la gestión de los datos generados por estas entidades. Está basada en la [Guía para la identificación y uso de entidades interoperables](https://paquete-apertura-datos.readthedocs.io/es/stable/guia_interoperables.html) elaborada por el equipo de la Dirección Nacional de Datos e Información Pública de la Secretaría de Gobierno de Modernización de la Jefatura de Gabinete de Ministros de la Nación. 

## Objetivo de esta guía

Esta es una **guía de buenas prácticas para el uso de entidades interoperables** para datos del Gobierno de la Ciudad Autónoma de Buenos Aires (GCABA). Se trata de datos básicos y fundamentales cuyo uso se repite frecuentemente entre datasets de temáticas y fuentes distintas.

Para hacer estas recomendaciones, nos basamos en la [guía del Gobierno Nacional](https://paquete-apertura-datos.readthedocs.io/es/stable/guia_interoperables.html), en estándares usados a nivel nacional e internacional y en la experiencia de trabajo del equipo de la Dirección General de Calidad Institucional y Gobierno Abierto, de la Subsecretaría de Gestión Estratégica y Calidad Institucional, Secretaría General y Relaciones Institucionales del Gobierno de la Ciudad Autónoma de Buenos Aires.

Esta es **una guía colaborativa y en progreso**. Valoramos, y alentamos, a organizaciones y ciudadanos a plantear ideas, sugerencias, y comentarios que nos ayuden a crear un mejor documento.

Para una discusión sobre la estandarización de datos, recomendamos consultar la **[Guía para la publicación de datos en formatos abiertos de la Ciudad de Buenos Aires](guia-abiertos.md)**. Este documento se complementa con esa guía y la **[Guía para el uso y la publicación de metadatos de la Ciudad de Buenos Aires](guia-metadatos.md)**.

## Datos de entidades interoperables

### ¿Qué son?

Las entidades interoperables **son aquellas que se repiten y usan frecuentemente** **dentro de datasets de**:

* **Temáticas diversas entre sí**.

* **Una misma temática** (ej.: Salud), **pero no de otras** (como Educación, Economía, Transporte, etc).

La mayoría de los datasets incluyen campos que responden al dónde, quién, cuándo y qué. Estos campos permiten que los datasets sean interoperables entre sí.

Veamos un ejemplo. Una matriz origen-destino de pasajeros de transporte urbano que dice cuántos viajes se hacen desde la fracción censal A a la fracción censal B, puede interoperar con datos del Censo Nacional sobre las personas que viven en A o en B (desocupación, edad, condiciones de la vivienda, actividad laboral, etc.). Decimos entonces, que la fracción censal es una entidad interoperable.

Algunos ejemplos de entidades interoperables pueden ser:

* **Transversales** (afectan a la mayoría de las áreas temáticas)

    * **¿Dónde?**: geografía (países, provincias, departamentos, fracciones censales, barrios, comunas, direcciones, códigos postales, plazas).

    * **¿Quién?**: personas (físicas, jurídicas). Entidades (niveles gubernamentales, organismos internacionales, otros países, sociedad civil).

    * **¿Qué?**: categorías presupuesto. Clasificación de bienes transables.

* **Específicas** (afectan a alguna/s área/s temática/s específica/s)

    * **¿Qué?**: actividades económicas. Clasificación de enfermedades. Clasificación de términos clínicos. Clasificación de unidades educativas.

### ¿Por qué es importante estandarizarlos?

**Las entidades interoperables son las que permiten que los datasets hablen entre sí**, pero **esto no puede suceder cuando dos datasets nombran de forma distinta** a una misma entidad interoperable (como cuando se usan distintos sistemas de *ids* o se nombra una misma entidad con/sin mayúsculas, usando artículos y preposiciones (o no usándolos), usando abreviaturas, siglas, tildes, forma corta o completa de un nombre, etc.

Para que los datasets puedan ser interoperables, **deben identificarse todas las entidades interoperables presentes en un dataset y asegurarse de que los datos sobre ellas siguen el mismo estándar**.

A continuación, **proponemos una selección de estándares** siguiendo los producidos por organismos de la Administración Pública Nacional y otros definidos por el Gobierno de la Ciudad Autónoma de Buenos Aires para identificación y uso de entidades interoperables presentes en un activo de datos, en algunas categorías transversales a varias áreas temáticas. **Recomendamos con énfasis usarlos** en todos aquellos casos en los que estén presentes esas entidades. Si por algún motivo esto fuera difícil de aplicar, sugerimos crear un diccionario que permita la traducción de estándares propios a los recomendados.

En los casos de **entidades interoperables específicas sobre alguna temática**, recomendamos **usar el estándar más difundido entre quienes trabajan con frecuencia sobre esa temática**.

**Cuando no existan** estándares claros para algún tipo de entidad interoperable en particular, sugerimos **adoptar el mejor estándar internacional en uso**, y seguirlo en forma consistente en todos los datasets que genere el organismo.

**La adopción de estándares** para el uso de datos de entidades interoperables está **sujeto a cambios y versionados. Por eso, siempre es importante comunicarlos** en forma clara y consistente.

Consideramos a los estándares que recomendamos en este documento como suficientemente estables, abarcativos, difundidos y mantenidos como para que su uso sea beneficioso para el aprovechamiento de los datos y su adopción transparente.

## Tipos de entidades interoperables

### Geográficas

#### Países o territorios internacionales

Siguiendo los lineamientos definidos para la Administración Pública Nacional, los nombres y códigos de países o territorios internacionales deben seguir el estándar [ISO 3166-1](https://es.wikipedia.org/wiki/ISO_3166-1). Recomendamos que el dataset contenga un campo con el código alfabético de 3 dígitos del estándar (Código alfa-3) y otro con el nombre completo del país en español. Para esto, recomendamos usar los "Nombres de uso común" de la [lista de países y sus códigos alfa-3 que publica INDEC](http://www.indec.gov.ar/ftp/cuadros/territorio/codigo_paises.xls).

En esta guía, elegimos incluir los nombres de países oficiales y en castellano. Sin embargo, la denominación de los países varía de acuerdo al idioma que se utilice. Por eso, hacemos énfasis en la necesidad de incluir el código de país según el estándar ISO 3166, que es ampliamente usado por organismos internacionales.

A modo de ejemplo, en la Argentina nos referimos a uno de nuestros países vecinos coloquialmente como "Brasil", mientras que el nombre oficial en portugués es “República Federativa do Brasil” y la traducción oficial en español “República Federativa del Brasil”. El código de país según el estándar definido es “BRA” lo cual resuelve el problema de denominación.

Se recomienda también que el nombre del campo del código sea "pais_id" o, en el caso de que haya más de un campo “país” en el dataset, el nombre de cada campo finalice con “pais_id” (Ej.: “desde_pais_id”, “hasta_pais_id”), mientras que el campo con el nombre completo del país debería ser “pais_nombre”.

<span class="no-recomendado">**No recomendado**</span>

<table>
<tbody>
  <tr>
    <td>pais_origen</td>
    <td>pais_destino</td>
    <td>valor_usd</td>
  </tr>
  <tr>
    <td>Argentina</td>
    <td>China</td>
    <td>1405678</td>
  </tr>
  <tr>
    <td>República Popular China</td>
    <td>argentina</td>
    <td>2456786</td>
  </tr>
</tbody>
</table>

<span class="recomendado">**Recomendado**</span>

<table>
 <colgroup>
    <col style="width:18%">
    <col style="width:22%">
    <col style="width:18%">
    <col style="width:24%">
    <col style="width:18%">
  </colgroup>
<tbody>
  <tr>
    <td>origen_pais_id</td>
    <td>origen_pais_nombre</td>
    <td>destino_pais_id</td>
    <td>destino_pais_nombre</td>
    <td>valor_usd</td>
  </tr>
  <tr>
    <td>ARG</td>
    <td>Argentina</td>
    <td>CHN</td>
    <td>China</td>
    <td>1405678</td>
  </tr>
  <tr>
    <td>CHN</td>
    <td>China</td>
    <td>ARG</td>
    <td>Argentina</td>
    <td>2456786</td>
  </tr>
</tbody>
</table>


#### Divisiones o unidades territoriales internas

En el caso de las divisiones o unidades territoriales internas, recomendamos usar el sistema de identificadores de la cartografía censal del Censo Nacional 2010 del Instituto Nacional de Estadística y Censos ([listado de códigos](https://redatam.indec.gob.ar/redarg/CENSOS/CPV2010rad/Docs/codigos_provincias.pdf) y [explicación metodológica](http://geoservicios.indec.gov.ar/codgeo/index.php?pagina=definiciones)) que incluye identificadores numéricos compuestos de una cantidad fija de dígitos (el tipo de datos debe ser textual, ya que tiene ceros a la izquierda que son significativos) para, entre otras, las siguientes entidades interoperables:

* Provincias ([CSV](http://www.ign.gob.ar/descargas/geodatos/departamento.csv) | [SHP](http://www.ign.gob.ar/descargas/geodatos/provincia.zip) | [GEOJSON](http://www.ign.gob.ar/descargas/geodatos/provincia_geojson.zip))
* [Comunas](https://data.buenosaires.gob.ar/api/files/comunas.csv/download)
* [Barrios](https://data.buenosaires.gob.ar/api/files/barrios.csv/download)
* Fracciones Censales
* Radios Censales

Cabe aclarar que las fracciones censales, la cobertura geográfica, los nomencladores y codificación de INDEC son referencias dinámicas, ya que pueden llegar a modificarse en los censos. Las incluidas en esta guía refieren al Censo Nacional de Población, Hogares y Viviendas 2010.

¿Cómo se relacionan estas entidades entre sí? Veremos que estas unidades pueden ordenarse jerárquicamente de modo tal que algunas contienen a las otras, aunque no en todos los casos. A continuación, explicamos los conjuntos de entidades que conforman una jerarquía internamente consistente.

##### A. Comunas -> Barrios -> Fracciones Censales -> Radios Censales (CBFR)

La Ciudad de Buenos Aires constituye una **excepción** a la regla PDL (partido- departamento- localidad), utilizada a nivel nacional, ya que es una localidad compuesta por departamentos (comunas), de manera que no puede componerse identificador compuesto de tipo provincia-departamento-localidad. Para este caso, recomendamos usar el identificador de jurisdicción de primer nivel de la Ciudad de Buenos Aires ("02").

**Las comunas son las jurisdicciones de primer orden** que marcan la división de la Ciudad Autónoma de Buenos Aires. El territorio municipal se divide en 15  comunas, siendo que algunos territorios pueden ser marcados como “Indeterminado” (98) o “Sin declarar-Desconocido-Ignorado” (99).

La generación de los límites de comunas se basó en la [Ordenanza Nº 23.698 (11 de junio de 1968)](https://boletinoficial.buenosaires.gob.ar/normativaba/norma/84707) completada por la [Ordenanza Nº 26607 de 1972](https://boletinoficial.buenosaires.gob.ar/normativaba/norma/53431).

En Septiembre 2006 la modificación en base a la [Ley Nº 1.777](http://www.buenosaires.gob.ar/areas/leg_tecnica/sin/normapop09.php?id=77544&qu) y sus modificatorias que redefine los límites de los Barrios de la Ciudad y deroga la Ordenanza 26.607 de 1972. En Noviembre 2006 se delimitaron los nuevos límites de Barrios según Ley Nº 1.777 generados por la Dirección General Electoral. En Junio 2007 ocurrió la última modificación a la Ley Nº 1777. Fue sancionada como [Ley Nº 2329](http://www.buenosaires.gob.ar/areas/leg_tecnica/sin/normapop09.php?id=99619&qu=c&ft=0&cp=&rl=0&rf=0&im=&ui=0&printi=&pelikan=1&sezion=825352&primera=0&mot_toda=&mot_frase=comunas&mot_alguna=) del 10/5/07, promulgada por Decreto Nº 779/07 del 01/06/2007. En Abril 2008 la última modificación a la Ley de Comunas 1.777 fue publicada en el Boletín Oficial Nº 2.910 del 16/04/2008.  Fue sancionada como Ley Nº 2.560/08. En Diciembre del 2011 se ajustaron los límites de cada barrio a la última versión de la topología de las calles de CABA.

**Una comuna se subdivide a su vez en jurisdicciones de segundo orden** llamadas [barrios](https://data.buenosaires.gob.ar/dataset/barrios).

La concepción de los límites de barrios fue digitalizada sobre los ejes de calle producto de la restitución del vuelo aerofotogramétrico de 1997 y, actualizaciones en base a los límites establecidos por Ordenanza N° 23.698 del 11 de junio de 1968, completada por la Ordenanza Nº 26607 de 1972.

Dicha Ley y sus modificatorias fueron derogadas y se redefinieron los nuevos límites por Ley Nº1777. Modificado a Abril de 2008, en base a la Ley Nº 2.650/08 que establece los nuevos límites de Barrios. En Diciembre del 2011 se ajustaron los límites de cada barrio a la última versión de la topología de las calles de CABA.

**Un barrio, a su vez, se puede subdividir en fracciones censales**, mientras que una [fracción censal se subdivide en radios censales](https://data.buenosaires.gob.ar/dataset/informacion-censal-por-radio). Estas son unidades censales que forman parte de la estructura de relevamiento censal.

El tamaño de las fracciones y los radios en áreas urbanas se determina según la cantidad de viviendas. La fracción tiene un promedio de 5000 viviendas mientras que el radio tiene un promedio de 300 a 500, considerando que no es posible dividir una manzana aunque supere este promedio.

Respecto a las Fracciones y Radios Censales, los mismos siguen la metodología generada por INDEC, teniendo la siguiente lógica de generación considerando el código de provincia como “02” y las comunas de la siguiente tabla: 

<table>
<tbody>
  <tr>
    <td>Código</td>
    <td>Comuna</td>
  </tr>
  <tr>
    <td>007</td>
    <td>1</td>
  </tr>
  <tr>
    <td>014</td>
    <td>2</td>
  </tr>
  <tr>
    <td>021</td>
    <td>3</td>
  </tr>
  <tr>
    <td>028</td>
    <td>4</td>
  </tr>
  <tr>
    <td>035</td>
    <td>5</td>
  </tr>
  <tr>
    <td>042</td>
    <td>6</td>
  </tr>
  <tr>
    <td>049</td>
    <td>7</td>
  </tr>
  <tr>
    <td>056</td>
    <td>8</td>
  </tr>
  <tr>
    <td>063</td>
    <td>9</td>
  </tr>
  <tr>
    <td>070</td>
    <td>10</td>
  </tr>
  <tr>
    <td>077</td>
    <td>11</td>
  </tr>
  <tr>
    <td>084</td>
    <td>12</td>
  </tr>
  <tr>
    <td>091</td>
    <td>13</td>
  </tr>
  <tr>
    <td>098</td>
    <td>14</td>
  </tr>
  <tr>
    <td>105</td>
    <td>15</td>
  </tr>
</tbody>
</table>

Cabe aclarar que los barrios no integran la codificación de estas unidades pero tienen coincidencia geográfica.

Los identificadores de cada una de estas divisiones se componen, sucesivamente, así:

<table id="identificadores-geograficos">
  <tr>
    <td><bold>provincia</bold><br/>
    2 dígitos<br/>
    "02"<br/>
    CABA
    </td>
    <td><bold>comuna</bold><br/>
    5 dígitos<br/>
    "02007"<br/>
    Comuna 1
    </td>
    <td><bold>fracción censal</bold><br/>
    7 dígitos<br/>
    "0200702"
    </td>
    <td><bold>radio censal</bold><br/>
    9 dígitos<br/>
    "020070201"
    </td>
  </tr>
</table>


* **Provincia**: 2 dígitos. Ej.: "02" es la "Ciudad Autónoma de Buenos Aires".

* **Comuna**: 5 dígitos. - Ej.: "02007" es la Comuna 1 de la “Ciudad Autónoma de Buenos Aires”.

* **Fracciones censales**: 7 dígitos. - Ej.: "0200702" es una Fracción Censal de la Comuna 1 de la “Ciudad Autónoma de Buenos Aires”.

* **Radios censales**: 9 dígitos. - Ej.: "020070201" es un Radio Censal de la Fracción Censal “0200702” de la Comuna 1 de la “Ciudad Autónoma de Buenos Aires”.

##### B. Villas -> [Unidades Territoriales de Inclusión Urbana](https://data.buenosaires.gob.ar/dataset/unidades-territoriales-de-inclusion-urbana)

A desarrollar

##### C. Otros nomencladores (espacios verdes, escuelas, centros de salud)

A desarrollar

##### D. ¿Cómo nombrar los campos?

Al igual que en el caso de los países o territorios internacionales, el dataset debe contener un campo con el código de la división o unidad territorial interna y otro con el nombre o descripción (en caso de que la tenga, anteriormente dijimos que las fracciones y radios censales no tienen nombre o descripción).

Los nombres de los campos identificadores deben ser, respectivamente:

* "provincia_id"
* "departamento_id"
* "fraccion_id"
* "radio_id"
* "municipio_id"
* "localidad_id"
* "aglomerado_id"

Análogamente, debe reemplazarse "_id" por “_nombre” para nombrar los campos que contiene el nombre de cada entidad, cuando esta lo tiene.

Resaltamos la importancia de que el tipo de datos del campo de un identificador es "textual" y no “numérico”. Esto es así porque un valor de tipo numérico no podría comenzar con ceros.

<span class="no-recomendado">**No recomendado**</span>

<table>
<tbody>
  <tr>
    <td>provincia</td>
    <td>flujo_comercial_tipo</td>
    <td>valor_usd</td>
  </tr>
  <tr>
    <td>Ciudad de Buenos Aires</td>
    <td>Exportación</td>
    <td>44949874</td>
  </tr>
  <tr>
    <td>CABA</td>
    <td>Importación</td>
    <td>44040711</td>
  </tr>
</tbody>
</table>


<span class="recomendado">**Recomendado**</span>

<table>
<tbody>
  <tr>
    <td>provincia_id</td>
    <td>provincia_nombre</td>
    <td>flujo_comercial_tipo</td>
    <td>valor_usd</td>
  </tr>
  <tr>
    <td>02</td>
    <td>CABA</td>
    <td>Exportación</td>
    <td>44949874</td>
  </tr>
  <tr>
    <td>02</td>
    <td>CABA</td>
    <td>Importación</td>
    <td>44040711</td>
  </tr>
</tbody>
</table>


#### Direcciones y lugares

Siempre que sea posible, cuando un dataset contenga información que identifica a un punto en el espacio geográfico, recomendamos incluir las coordenadas de la manera establecida en la tercera tabla. Las coordenadas de un punto deben ser números decimales negativos o positivos contenidos en dos campos llamados "lat" y long.

Si el dataset contiene información sobre direcciones (especialmente en los casos en los que no sea posible proveer coordenadas), recomendamos incluir:

* "calle_nombre"
* "calle_altura"
* "barrio"
* "comuna"
* "codigo_postal"
* "codigo_postal_argentino"
* "localidad_id"
* "localidad_nombre"
* "provincia_id"
* "provincia_nombre"

Si el dataset incluye direcciones fuera del territorio argentino, deben además incluirse:

* "pais_id"
* "pais_nombre"

Para normalizar las direcciones de la CABA, recomendamos utilizar el servicio del [Normalizador de direcciones CABA](http://usig.buenosaires.gob.ar/) de la Unidad de Sistemas de Información Geográfica (USIG) del Gobierno de la Ciudad Autónoma de Buenos Aires.

<span class="no-recomendado">**No recomendado**</span>

<table>

<tbody>
  <tr>
    <td>lugar_nombre</td>
    <td>calle_nombre</td>
    <td>calle_altura</td>
    <td>ciudad</td>
  </tr>
  <tr>
    <td>Teatro Colón</td>
    <td>Cerrito</td>
    <td>604</td>
    <td>Ciudad Autónoma de Buenos Aires, CABA</td>
  </tr>
</tbody>
</table>


**Aceptable 1** - sólo dirección normalizada

<table>
 <colgroup>
    <col style="width:14%">
    <col style="width:14%">
    <col style="width:14%">
    <col style="width:14%">
     <col style="width:15%">
    <col style="width:13%">
    <col style="width:16%">
  </colgroup>
<tbody>
  <tr>
    <td style="font-size:11px;">lugar_nombre</td>
    <td style="font-size:11px;">calle_nombre</td>
    <td style="font-size:11px;">calle_altura</td>
    <td style="font-size:11px;">localidad_id</td>
    <td style="font-size:11px;">localidad_nombre</td>
    <td style="font-size:11px;">provincia_id</td>
    <td style="font-size:11px;">provincia_nombre</td>
  </tr>
  <tr>
    <td>Teatro Colón</td>
    <td>Cerrito</td>
    <td>604</td>
    <td>02001010</td>
    <td style="font-size:11px;">CABA</td>
    <td>02</td>
    <td style="font-size:11px;">CABA</td>
  </tr>
</tbody>
</table>


**Aceptable 2** - sólo coordenadas

<table>
<tbody>
  <tr>
    <td>lugar_nombre</td>
    <td>lat</td>
    <td>long</td>
  </tr>
  <tr>
    <td>Teatro Colón</td>
    <td>-34.601041</td>
    <td>-58.383079</td>
  </tr>
</tbody>
</table>


**Aceptable 3** - dirección con esquina

<table>
 <colgroup>
    <col style="width:14%">
    <col style="width:14%">
    <col style="width:14%">
    <col style="width:14%">
     <col style="width:15%">
    <col style="width:13%">
    <col style="width:16%">
  </colgroup>
<tbody>
  <tr>
    <td style="font-size:11px;">lugar_nombre</td>
    <td style="font-size:11px;">calle_nombre</td>
    <td style="font-size:11px;">calle_cruce</td>
    <td style="font-size:11px;">localidad_id</td>
    <td style="font-size:11px;">localidad_nombre</td>
    <td style="font-size:11px;">provincia_id</td>
    <td style="font-size:11px;">provincia_nombre</td>
  </tr>
  <tr>
    <td>Teatro Colón</td>
    <td>Cerrito</td>
    <td>Tucumán</td>
    <td>02001010</td>
    <td style="font-size:11px;">CABA</td>
    <td>02</td>
    <td style="font-size:11px;">CABA</td>
  </tr>
</tbody>
</table>


<span class="recomendado">**Recomendado**</span> - coordenadas y dirección normalizada

<table>
<tbody>
  <tr>
    <td  style="font-size:11px;">lugar_nombre</td>
    <td style="font-size:11px;">calle_nombre</td>
    <td style="font-size:11px;">calle_altura</td>
    <td style="font-size:11px;">localidad_id</td>
    <td style="font-size:11px;">localidad_nombre</td>
    <td style="font-size:11px;">provincia_id</td>
    <td style="font-size:11px;">provincia_nombre</td>
    <td style="font-size:11px;">lat</td>
    <td style="font-size:11px;">long</td>
  </tr>
  <tr>
    <td style="font-size:10px;">Teatro Colón</td>
    <td style="font-size:9px;">Cerrito</td>
    <td style="font-size:10px;">604</td>
    <td style="font-size:10px;">02001010</td>
    <td style="font-size:10px;">CABA</td>
    <td style="font-size:10px;">02</td>
    <td style="font-size:10px;">CABA</td>
    <td style="font-size:10px;">-34.601041</td>
    <td style="font-size:10px;">-58.383079</td>
  </tr>
</tbody>
</table>


#### **Códigos postales**

Los códigos postales deben estar contenidos en un campo llamado "codigo_postal" y seguir el formato definido por el Correo Argentino para el [Código Postal Argentino (CPA)](http://www.correoargentino.com.ar/formularios/cpa) a partir de la competencia asignada por la Secretaría de Comunicaciones mediante la Resolución N° 1368/98. Cuando se haga referencia al CPA, el campo deberá llamarse "codigo_postal_argentino". 

El CPA amplía la información del código postal, incorporando 4 letras que permiten identificar cada cara de manzana en las localidades de más de 500 habitantes. Las localidades de menos de 500 habitantes poseen un único CPA.

El CPA se compone de:

* 1 letra: Identifica a la Provincia.
* 4 números: El Código Postal tradicional.
* 3 letras: Identifican a la Cara de la Manzana.

Ej.: C1426BMD

<span class="no-recomendado">**No recomendado**</span>

<table  id="una-columna">
<tbody>
  <tr>
    <td>codigo_postal</td>
  </tr>
  <tr>
    <td>1426</td>
  </tr>
  <tr>
    <td>C 1426 BMD</td>
  </tr>
  <tr>
    <td>c1426bmd</td>
  </tr>
  <tr>
    <td>C1426</td>
  </tr>
</tbody>
</table>


<span class="recomendado">**Recomendado**</span>

<table id="una-columna">
<tbody>
  <tr>
    <td>codigo_postal_argentino</td>
  </tr>
  <tr>
    <td>C1426BMD</td>
  </tr>
  <tr>
    <td>C1426BMD</td>
  </tr>
  <tr>
    <td>C1426BMD</td>
  </tr>
  <tr>
    <td>C1426BMD</td>
  </tr>
</tbody>
</table>


### **Personas físicas**

Las personas físicas deben identificarse por su nombre completo separado en dos campos ("nombre" y “apellido”), cuando sea posible, donde deben consignarse todos los nombres y todos los apellidos que identifican a un individuo en su documento de identidad oficial, sea el que corresponda según el individuo se presente como residente nacional o extranjero.

Así mismo, recomendamos (de ser posible) agregar dos columnas "id" y “tipo_id” que respectivamente contengan el número o cadena de caracteres que constituye el identificador del documento oficial de la persona y el tipo de documento oficial al que este identificador corresponde (Ej.: DNI, LE, LC y Pasaporte).

Esto es sencillo en el caso de residentes nacionales, pero la variedad de tipos de documentos oficiales que puede presentar un residente extranjero es mucho más amplia y difícil de abarcar. En este último caso es suficiente con consignar si el documento es un "Pasaporte" u “Otro”. Adicionalmente, si el dataset puede contener datos de individuos de diferentes nacionalidades recomendamos agregar un campo “_pais” que contenga la nacionalidad del individuo de referencia.

Tal como explicamos en el caso de países o territorios internacionales, si hubiera más de un campo relativo a "personas" o la mera nomenclatura “nombre” pudiera prestarse a confusión, los campos correspondientes serán compuestos. Ejemplo:

* "sujeto_obligado_nombre"
* "sujeto_obligado_apellido"
* "sujeto_obligado_id"
* "sujeto_obligado_tipo_id"
* "sujeto_obligado_pais_id"
* "sujeto_obligado_pais_nombre"
* "representante_nombre"
* "representante_apellido"
* "representante_id"
* "representante_tipo_id"

<span class="no-recomendado">**No recomendado**</span>

<table>
<tbody>
  <tr>
    <td>sujeto_obligado</td>
    <td>representante</td>
  </tr>
  <tr>
    <td>José Pérez</td>
    <td>Carlos Gómez</td>
  </tr>
  <tr>
    <td>josé Pérez</td>
    <td>Carlos J. Gómez</td>
  </tr>
  <tr>
    <td>Pérez, José</td>
    <td>Gómez, Carlos</td>
  </tr>
  <tr>
    <td>Pérez, José</td>
    <td>Gómez, Carlos J.</td>
  </tr>
</tbody>
</table>


**Aceptable**

<table>
<tbody>
  <tr>
    <td  style="font-size:11px;">sujeto_obligado_nombre</td>
    <td style="font-size:11px;">sujeto_obligado_apellido</td>
    <td style="font-size:11px;">representante_nombre</td>
    <td style="font-size:11px;">representante_apellido</td>
  </tr>
  <tr>
    <td>José</td>
    <td>Pérez</td>
    <td>Carlos Jorge</td>
    <td>Gómez</td>
  </tr>
  <tr>
    <td>José</td>
    <td>Pérez</td>
    <td>Carlos Jorge</td>
    <td>Gómez</td>
  </tr>
  <tr>
    <td>José</td>
    <td>Pérez</td>
    <td>Carlos Jorge</td>
    <td>Gómez</td>
  </tr>
  <tr>
    <td>José</td>
    <td>Pérez</td>
    <td>Carlos Jorge</td>
    <td>Gómez</td>
  </tr>
</tbody>
</table>


<span class="recomendado">**Recomendado**</span>

<table>
<colgroup>
    <col style="width:20%">
    <col style="width:15%">
    <col style="width:15%">
    <col style="width:15%">
    <col style="width:15%">
    <col style="width:20%">
  </colgroup>
  <tbody>
  <tr>
    <td style="font-size:10px;">sujeto_obligado_nombre</td>
    <td style="font-size:10px;">sujeto_obligado_apellido</td>
    <td style="font-size:10px;">sujeto_obligado_id</td>
    <td style="font-size:10px;">sujeto_obligado_tipo_id</td>
    <td style="font-size:10px;">sujeto_obligado_pais_id</td>
    <td style="font-size:10px;">sujeto_obligado_pais_nombre</td>
  </tr>
  <tr>
    <td>José</td>
    <td>Pérez</td>
    <td style="font-size:10px;">11111111</td>
    <td>DNI</td>
    <td>ARG</td>
    <td>Argentina</td>
  </tr>
  <tr>
    <td>José</td>
    <td>Pérez</td>
    <td style="font-size:10px;">11111111</td>
    <td>DNI</td>
    <td>ARG</td>
    <td>Argentina</td>
  </tr>
  <tr>
    <td>José</td>
    <td>Pérez</td>
    <td style="font-size:10px;">11111111</td>
    <td>DNI</td>
    <td>ARG</td>
    <td>Argentina</td>
  </tr>
  <tr>
    <td>José</td>
    <td>Pérez</td>
    <td style="font-size:10px;">11111111</td>
    <td>DNI</td>
    <td>ARG</td>
    <td>Argentina</td>
  </tr>
</tbody>
</table>

### **Perspectiva de Género**

En el espíritu de lo establecido por la [Ley Nº 91 de 1998](https://www.buenosaires.gob.ar/areas/leg_tecnica/sin/normapop09.php?id=919&qu=c&ft=0&cp=&rl=1&rf=0&im=&ui=0&printi=1&pelikan=1&sezion=2316523&primera=0&mot_toda=&mot_frase=&mot_alguna=) y la [Ley Nº 5.924 de 2017](http://www2.cedom.gob.ar/es/legislacion/normas/leyes/ley5924.html), ambas sancionadas por la Legislatura de la CABA, **todos los datos que refieran a personas físicas deben estar desagregados por sexo y género.** 

A tales efectos, **todas las bases de datos abiertos del GCBA cuyas unidades de análisis sean personas físicas deberán incluir los campos “sexo” y “género”.**

1. La variable **sexo** refiere al sexo al momento del nacimiento de la persona; es decir, el sexo biológico asignado al nacer.
Siguiendo lo establecido por la norma [ISO 5218](https://www.iso.org/standard/36266.html), debe ser categorizada de la siguiente manera:
  
    * "Varón"
    * "Mujer"

2. La variable **género** refiere a la identidad de género de la persona; es decir, la expresión de género con la cual una persona se identifica y autorreconoce. 
  Debe ser categorizada de la siguiente manera:

    * “Varón”
    * “Mujer”
    * “Varón trans”
    * “Mujer trans”
    * “Travesti”
    * “Otro”

3. Las variables **“sexo”** y **“género”** no son intercambiables. Ambas variables deben ser incluidas en la sistematización y publicación de todos los datos que refieren a personas físicas, incluso cuando los valores de ambas variables coincidan o haya valores para sólo una de ellas. 

4. La variable **“sexo”** debe continuar presente en todas las bases de datos, ya que de otra manera se imposibilitaría la comparabilidad con datos sistematizados en el pasado. 

5. No confundir **“sexo”** o **“género/identidad de género”** con **“orientación sexual”** (atracción emocional y/o sexual que una persona mantiene hacia otra), en caso de que tal categoría existiese en una base de datos. De ser así, debe crearse un nuevo campo con el nombre “orientación sexual”. 

Para más información al respecto podés consultar:

- [Ley N° 91/2008: Consignación de variables de sexo y edad en la Ciudad de Buenos Aires](https://www.buenosaires.gob.ar/areas/leg_tecnica/sin/normapop09.php?id=919&qu=c&ft=0&cp=&rl=1&rf=0&im=&ui=0&printi=1&pelikan=1&sezion=2316523&primera=0&mot_toda=&mot_frase=&mot_alguna=)
- [Ley N° 474/2000: Plan de Igualdad real de oportunidades y de trato entre mujeres y varones](http://www2.cedom.gov.ar/es/legislacion/normas/leyes/ley474.html)
- [Ley N° 5924/2007: Incorporación de enfoque de género en las producciones estadísticas de la Ciudad de Buenos Aires](http://www2.cedom.gov.ar/es/legislacion/normas/leyes/ley474.html)
- [Marco de referencia del SIGBA](https://www.estadisticaciudad.gob.ar/eyc/wp-content/uploads/2018/05/marco_referencia_SIGBA.pdf)
- [Nuevas realidades, nuevas demandas. Desafíos para la medición de la identidad de género en el Censo de Población (INDEC, 2019)](https://www.indec.gob.ar/ftp/cuadros/publicaciones/identidad_genero_censo_2020.pdf)
- [Australian Government Guidelines on the Recognition of Sex and Gender (2015)](https://www.ag.gov.au/Publications/Documents/AustralianGovernmentGuidelinesontheR
ecognitionofSexandGender/AustralianGovernmentGuidelinesontheRecognitionofSexandGender.PDF)

### **Personas jurídicas**

Las entidades con personería jurídica local (Ej.: empresas argentinas, ONGs argentinas, etc.) deben registrarse con su CUIT y razón social. Por ejemplo:

* "exportador_cuit"
* "exportador_razon_social"

<span class="no-recomendado">**No recomendado**</span>

<table id="una-columna">
<tbody>
  <tr>
    <td>exportador</td>
  </tr>
  <tr>
    <td>Los Tomates Andinos</td>
  </tr>
  <tr>
    <td>Los Tomates</td>
  </tr>
  <tr>
    <td>Los Tomates Andinos SRL</td>
  </tr>
  <tr>
    <td>Tomates Andinos</td>
  </tr>
</tbody>
</table>


<span class="recomendado">**Recomendado**</span>

<table>
<tbody>
  <tr>
    <td>exportador_cuit</td>
    <td>exportador_razon_social</td>
  </tr>
  <tr>
    <td>33111111117</td>
    <td>Los Tomates Andinos SRL</td>
  </tr>
  <tr>
    <td >33111111117</td>
    <td>Los Tomates Andinos SRL</td>
  </tr>
  <tr>
    <td >33111111117</td>
    <td>Los Tomates Andinos SRL</td>
  </tr>
  <tr>
    <td >33111111117</td>
    <td>Los Tomates Andinos SRL</td>
  </tr>
</tbody>
</table>


Si el dataset sólo contiene personas jurídicas registradas en la jurisdicción argentina, el enfoque recomendado para nombrar los campos es el de agregar "_cuit" y “_razon_social” ya que es una nomenclatura específica mucho más descriptiva para el usuario que “_id” y “_desc”. Da cuenta del tipo de “_id” de que se trate y del tipo de descripción asociada.

La Administración Federal de Ingresos Públicos (AFIP) mantiene un [padrón actualizado](http://www.afip.gov.ar/genericos/cinscripcion/archivocompleto.asp) de todas las personas jurídicas que tienen un CUIT registrado en esa dependencia, que puede ser usado para normalizar o buscar la razón social.

En el caso de que el dataset pueda contener personas jurídicas fuera de la jurisdicción argentina, recomendamos un enfoque análogo al tratamiento de personas físicas:

* "inversor_id"
* "inversor_tipo_id" (Ej.: en el caso de una empresa argentina sería “CUIT”)
* "inversor_desc"
* "inversor_pais_id"
* "inversor_pais_nombre"

<span class="recomendado">**Recomendado**</span>

<table>
 <colgroup>
    <col style="width:20%">
    <col style="width:20%">
    <col style="width:17%">
    <col style="width:20%">
    <col style="width:23%">
  </colgroup>
<tbody>
  <tr>
    <td>inversor_id</td>
    <td>inversor_tipo_id</td>
    <td>inversor_desc</td>
    <td>inversor_pais_id</td>
    <td>inversor_pais_nombre</td>
  </tr>
  <tr>
    <td style="font-size:11px;">33111111117</td>
    <td>CUIT</td>
    <td>Los Tomates Andinos SRL</td>
    <td>ARG</td>
    <td>Argentina</td>
  </tr>
  <tr>
    <td style="font-size:11px;">33111111117</td>
    <td>CUIT</td>
    <td>Los Tomates Andinos SRL</td>
    <td>ARG</td>
    <td>Argentina</td>
  </tr>
  <tr>
    <td style="font-size:11px;">1234567890</td>
    <td>TIN</td>
    <td>Tomatoes Inc.</td>
    <td>USA</td>
    <td>Estados Unidos</td>
  </tr>
  <tr>
    <td style="font-size:11px;">987654321</td>
    <td>Steuer-Id</td>
    <td>Tomate</td>
    <td>DEU</td>
    <td>Alemania</td>
  </tr>
</tbody>
</table>


Dependiendo de la forma de recolección de los datos, la temática particular del dataset y las capacidades del organismo responsable del mantenimiento del activo de datos, puede ser difícil la recolección comprehensible de "_id" y “_tipo_id” de las personas jurídicas de jurisdicción extranjera. Por eso, estos campos pueden llegar a quedar frecuentemente en blanco (valor ausente). Sin embargo, recomendamos con especial énfasis registrar el nombre (“_desc”) de la entidad en cuestión y el país bajo cuya jurisdicción se encuentra.


### **Entidades de Gobierno de la Ciudad Autónoma de Buenos Aires**

A desarrollar

## Glosario

Ver [Glosario](glosario.md)

