# Dónde vive la ley dominicana

La ley dominicana es pública y gratuita. El problema es que está repartida entre
cinco organismos que no se hablan entre sí, cada uno con su propio portal, su
propia forma de organizar y sus propios huecos.

Este es el mapa. Qué publica cada quién, en qué forma, cuánto hay y qué le falta.

No es el corpus: no hay documentos aquí. Es la respuesta a «¿dónde busco esto?»,
que es la pregunta que casi nadie tiene escrita.

## Las cinco fuentes

| Organismo | Qué publica | Volumen |
|---|---|---|
| **[Consultoría Jurídica del Poder Ejecutivo](https://consultoria.gov.do)** | Leyes, decretos, reglamentos, resoluciones | ~108,000 |
| **[Tribunal Constitucional](https://www.tribunalconstitucional.gob.do)** | Sentencias, resoluciones, extractos | desde 2012 |
| **[Senado — Memoria Histórica](https://memoriahistorica.senadord.gob.do)** | Contratos, resoluciones, expedientes | ~44,940 |
| **[Cámara de Diputados — SIL](https://www.diputadosrd.gob.do/sil/)** | Iniciativas, sesiones, comisiones | ~5,875 iniciativas |
| **[Juristeca — ENJ](https://juristeca.edu.do)** | Jurisprudencia, boletines, biblioteca | — |

El detalle completo, con metadatos disponibles y advertencias por fuente, está en
[`datos/fuentes.json`](datos/fuentes.json).

## Dónde buscar, según lo que necesites

**Una ley, un decreto o un reglamento** → Consultoría Jurídica. Es la fuente
central de la normativa vigente. Si solo vas a mirar un sitio, es este.

**Saber si algo es constitucional** → Tribunal Constitucional. Sus sentencias son
vinculantes y condicionan cómo se lee todo lo demás.

**Cómo se tramitó una ley: quién la propuso, cuándo se discutió, en qué quedó** →
SIL, de la Cámara de Diputados. Es el único que muestra el proceso y no solo el
resultado. Ojo: la documentación cuelga de la iniciativa o la sesión, así que
primero hay que ubicar a cuál pertenece.

**Jurisprudencia por criterio —órgano, tribunal, ponente, tipo de recurso—** →
Juristeca. Su clasificación por facetas no tiene equivalente en los demás
portales. Son **dos** portales y conviene no confundirlos:
[juristeca.edu.do](https://juristeca.edu.do) es el catálogo y
[jurisprudencia.enj.org](https://jurisprudencia.enj.org) el buscador de
jurisprudencia.

**El expediente documental de algo legislativo** → Memoria Histórica del Senado.
Es un archivo, no un catálogo de normas: ahí está el rastro en papel.

## Tres cosas que valen para todas

**Espera escaneos.** Una parte considerable de lo publicado son fotografías de
páginas sin capa de texto. En el fondo del Senado, en buena medida; en las
sentencias del TC y en Consultoría, en parte. Si vas a procesarlo con software,
cuenta con OCR desde el principio — hay una herramienta para decidir qué lo
necesita en [pdf-triage](https://github.com/johnnyvaldezcalderon/pdf-triage).

**Los enlaces caducan, los documentos no.** Consultoría se reconstruyó en 2026 y
las URL anteriores dejaron de resolver; Juristeca retiró su navegación HTML por
documento; el TC sirve los PDF desde almacenamiento externo. Si un enlace de hace
unos años a una norma dominicana está roto, lo más probable es que el documento
siga publicado y lo que cambió sea la dirección. Guarda el número y la fecha, no
la URL.

**Ninguna fuente te dice si algo sigue vigente.** Ni si fue derogado, ni si fue
modificado y por qué norma. Eso hay que reconstruirlo cruzando documentos, y es
con diferencia la parte más difícil de trabajar con esta documentación. No des
por vigente una norma porque aparezca publicada.

## Lo que falta, y no es poco

- **La Gaceta Oficial.** Los documentos de Consultoría citan su número de Gaceta,
  pero el texto de la Gaceta como publicación no está entre estas fuentes.
- **Lo municipal.** Las ordenanzas y resoluciones de los 158 municipios y 231
  distritos municipales no tienen repositorio central. Cada ayuntamiento publica
  por su cuenta, o no publica.
- **Lo sectorial.** Superintendencias, DGII, direcciones generales y reguladores
  publican en sus propios portales, con criterios distintos.

## Un detalle que ahorra horas

Las tablas de Consultoría traen **registros vacíos**: filas sin número, sin
título, sin Gaceta y sin fecha, para las que el origen responde 404 o 403. No son
documentos retirados ni fallos de red — no llegaron a existir.

Si estás midiendo cobertura, exclúyelos o las cifras salen infladas y vas a
perseguir errores que no lo son. A nosotros nos costó entenderlo.

## Qué NO incluye esto, y por qué

No hay endpoints, ni parámetros, ni cuerpos de petición, ni los rodeos concretos
para extraer en masa de cada portal.

Eso es deliberado y prefiero decirlo de frente: reunir esa parte costó mucho
trabajo y sostiene un producto. Lo que sí es de todos es saber **dónde está la
ley y en qué estado**, y eso está aquí completo. Un periodista, un investigador o
un estudiante que necesite ubicar un documento tiene con esto todo lo que
necesita.

Si trabajas en algo de interés público y te hace falta más, escribe y lo
conversamos.

## De dónde sale

De construir la ingesta de [ChatLeyes](https://chatleyes.com), que reúne y ordena
esta documentación para poder responder preguntas legales en español corriente.
Todo lo de aquí está comprobado contra los portales en vivo, no copiado de otra
documentación.

Si encuentras algo desactualizado —y va a pasar, estos portales cambian sin
avisar— abre un issue.

## Licencia

[CC BY 4.0](LICENSE) — Johnny Santiago Valdez Calderón. Úsalo, cítalo, cámbialo.
