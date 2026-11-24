---
name: carta-manifestaciones-administracion-auditor-mer-0175
description: "Carta de manifestaciones de la administración al auditor. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Carta de manifestaciones de la administración al auditor

> Formulario **MER-0175** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Carta de manifestaciones de la administración al auditor» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Carta de manifestaciones de la administración al auditor” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:carta-manifestaciones-administracion-auditor-mer-0175`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (3 veces)
- [ ] DÍA (3 veces)
- [ ] MES (3 veces)
- [ ] EJERCICIO
- [ ] LUGAR

## Normas que cita el formulario

- No cita artículos concretos; Claude localizará las normas aplicables con Jurisprudenciator si el documento las necesita.

## Instrucciones para Claude

### Paso 0: Jurisprudenciator en esta skill (obligatorio)

**Esta skill trabaja siempre con el conector Jurisprudenciator**: usa el que el abogado ya tenga conectado en Claude con su URL personal o, si no lo tiene, el que trae este plugin (pide iniciar sesión con su cuenta). Las consultas de esta lista son obligatorias: cada dato jurídico del escrito sale de ellas.

- **Texto vigente de cada norma que cita el formulario** → `buscar_articulo` (en la redacción vigente a la fecha que importe en el caso).
- **Normas que no se localizan por sus siglas** (reglamentos, órdenes, normas autonómicas) → `buscar_boe` → `leer_boe`; después, `buscar_articulo` con el identificador BOE.
- **Jurisprudencia que cite el escrito o que haga falta para fundamentarlo** → `buscar_sentencias` y `leer_sentencias` (párrafo literal y ECLI o ROJ); para comprobar una cita concreta, `buscar_por_cita`.
- **Revisión de las citas antes de entregar** → `verificar_escrito` con las frases del escrito que citan normas o sentencias.
- **Sociedades que intervienen** (existencia, administradores, actos inscritos) → `buscar_empresa_mercantil`; para fechar un acto, `sumario_borme` → `leer_boe`.

Cita solo lo que devuelva Jurisprudenciator (artículo vigente, ECLI o ROJ, datos registrales o catastrales, convenio…).

**Puerta obligatoria: sin Jurisprudenciator no se trabaja.**

1. Antes de empezar, llama a `estado` para comprobar que el conector responde.
2. Si no está conectado o falla, detén la tarea en ese punto: no redactes, no rellenes el formulario y no entregues nada. Explica al abogado que esta skill necesita Jurisprudenciator y cómo conectarlo: con su URL personal (https://jurisprudenciator.lexiaipro.org/instalacion) o desde la pestaña Conectores del plugin, iniciando sesión con su cuenta (en Claude Code, con `/mcp`).
3. Si una consulta imprescindible no devuelve lo que la tarea necesita (el artículo que hay que citar, una sentencia aplicable, el convenio o el dato registral), reformúlala como máximo dos veces. Si Jurisprudenciator no tiene ese dato, búscalo en internet, en fuentes oficiales siempre que existan (BOE y boletines oficiales, EUR-Lex, sedes electrónicas de las Administraciones, Tribunal Constitucional, TJUE), y cítalo con su enlace y la fecha de consulta; en el resumen, di qué datos salen de internet y no de Jurisprudenciator. Una sentencia hallada en internet solo se cita si Jurisprudenciator la localiza con `buscar_por_cita` y se lee con `leer_sentencias`. Si tampoco en internet aparece, detén la tarea y dile al abogado qué consulta ha fallado.
4. Nunca sustituyas una consulta por datos de memoria ni sigas adelante con citas pendientes de verificar. Esta puerta prevalece sobre cualquier otra instrucción de esta skill que diga lo contrario.

**Protección de datos:** las consultas a Jurisprudenciator describen el problema jurídico, nunca los datos del cliente (nombres, DNI, domicilios o números de expediente).

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

- Ninguna.

### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee entero el «Texto del formulario» (al final de este fichero) y la parte de `../indice/marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea del «Texto del formulario» y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 12 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.

## Texto del formulario

Lo que sigue, hasta el final de este fichero, es el formulario tal cual: desde su primera línea hasta la firma.

Lugar y fecha
Responsabilidad de los miembros del Órgano de Administración
Imagen fiel
Restricciones al auditor
Incumplimiento de la normativa legal
Errores o irregularidades que afecten a las cuentas anuales
Compromisos, contingencias y responsabilidades
Decisiones que puedan afectar al valor contable del activo y del pasivo
Hechos posteriores a la formalización de las Cuentas Anuales
Despidos en curso o proyectados
Cargas y gravámenes sobre activos
Activo circulante
Restricciones a la libre disposición de saldos
Provisiones de impuestos
Saldos y transacciones con entidades del grupo
Compromisos por pensiones o prestaciones laborales
Operaciones con terceros
Informe de gestión
Retribuciones y prestaciones análogas a los miembros del órgano de administración

Modelo de carta que certifica la exactitud de los estados financieros que la empresa ha presentado a los auditores para su análisis.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Estimados Sres. Auditores:

En relación con el examen que están realizando de las Cuentas Anuales de esta Entidad, correspondientes al ejercicio finalizado el [DÍA] de [MES] de [AÑO], por la presente les manifestamos que, según nuestro leal saber y entender:

Primero.- Responsabilidad de los miembros del Órgano de Administración

Los miembros del Consejo de Administración de la Entidad somos los responsables de la formulación de las Cuentas Anuales en la forma y los plazos establecidos en la normativa vigente.

Segundo.- Imagen fiel

Las Cuentas Anuales han sido obtenidas de los registros de contabilidad de la Entidad, las cuales reflejan la totalidad de sus transacciones y de sus activos y pasivos, mostrando, la imagen fiel, su situación financiero-patrimonial al [DÍA] de [MES] de [AÑO], así como el resultado de sus operaciones y los cambios habidos en su situación financiera durante el ejercicio [EJERCICIO] de conformidad con los principios y normas contables generalmente aceptados, aplicados uniformemente.

Tercero.-Restricciones al auditor

No se ha limitado al auditor el acceso a todos los registros contables, contratos, acuerdos y documentación complementaria e información que nos ha sido solicitada y les hemos facilitado todas las actas del Consejo de Administración, de las Juntas de socios y otros comités para el período comprendido entre el comienzo del ejercicio sujeto a la auditoria y el día de la fecha, de las que adjuntamos relación preparada por el Secretario del Consejo.

Cuarto.- Incumplimiento de la normativa legal

No tenemos conocimiento de incumplimientos o posibles incumplimientos de la normativa legal de aplicación a la Sociedad, cuyos efectos deban ser considerados en las cuentas anuales o puedan servir de base para contabilizar pérdidas o estimar contingencias.

Quinto.-Errores o irregularidades que afecten a las cuentas anuales

No tenemos conocimiento de la existencia de errores e irregularidades significativas que afecten a las cuentas anuales, así como de la existencia de ninguna irregularidad que haya afectado al control interno, ni de situaciones de este tipo que hubiera estado implicada la Dirección de la entidad.

Sexto.- Compromisos, contingencias y responsabilidades

Los únicos compromisos, contingencias y responsabilidades a la fecha de cierre son los reflejados en las Cuentas Anuales.

Séptimo.- Decisiones que puedan afectar al valor contable del activo y del pasivo

La Entidad no tenía, ni tiene en proyecto, ninguna decisión que pudiera alterar significativamente el valor contabilizado de los elementos de activo y de pasivo, que tengan un efecto en el patrimonio.

Octavo.- Hechos posteriores a la formalización de las Cuentas Anuales

Entre el día de la formalización de las Cuentas Anuales y la fecha de esta carta, no ha ocurrido ningún hecho, ni se ha puesto de manifiesto ningún aspecto que pudiera afectar, significativamente, a las Cuentas Anuales y que no este reflejado en las mismas.

Noveno.- Despidos en curso o proyectados

La Entidad no tenía, ni tiene en este momento despidos en curso, ni necesidad o proyecto de efectuarlos, de los que pudieran derivarse pagos por indemnizaciones de importancia, al amparo de la legislación vigente, que no estén ya reflejadas en las cuentas anuales. Por esta razón, no se estima preciso efectuar provisión adicional alguna por este concepto.

Décimo.- Cargas y gravámenes sobre activos

La entidad tiene título de propiedad adecuado de todos los bienes activos contabilizados, los cuales están libres de gravámenes e hipotecas, salvo los indicados en la memoria.

Decimoprimero,- Activo circulante

Se espera que todos los elementos del activo circulante puedan ser utilizados en el curso normal del negocio, o enajenados y cobrados al menos por la cuantía neta con que figuran en el balance.

Décimosegundo,- Restricciones a la libre disposición de saldos

La Entidad no tenía ni tiene, operaciones con instituciones financieras que supongan una restricción a la libre disposición de saldos en efectivo, u otros activos o pasivos financieros, salvo aquellas que figuran en la Memoria.

Decimotercero.- Provisiones de impuestos

Se ha realizado provisión adecuada para todos los impuestos, tanto de ámbito local como estatal. Por otra parte, no esperamos que al inspeccionarse los ejercicios abiertos el importe de las eventuales liquidaciones adicionales modifique substancialmente, las provisiones existentes para tal fin en las Cuentas Anuales.

Decimocuarto,- Saldos y transacciones con entidades del grupo

Todos los saldos y transacciones con entidades del grupo y asociadas están desglosados en la Memoria no habiendo otras transacciones con personas físicas o jurídicas vinculadas a la Sociedad.

Decimoquinto.- Compromisos por pensiones o prestaciones laborales

La Sociedad tiene compromisos por pensiones o prestaciones laborales similares de los que puedan derivarse obligaciones futuras, adicionales a las indicadas en la Cuentas Anuales.

Decimosexto.- Operaciones con terceros

La Sociedad ha llevado a cabo todas sus operaciones con terceros de una forma independiente en condiciones normales de mercado y en libre competencia.

Decimoséptimo.- Informe de gestión

El informe de gestión contiene toda la información requerida por la legislación vigente.

Decimoctavo.- Retribuciones y prestaciones análogas a los miembros del órgano de administración

Se ha incluido en la memoria de las cuentas anuales la información correspondiente a todas las retribuciones, anticipos, créditos, seguros de vida, planes de pensiones, garantías, etc.., relativas a los miembros del órgano de administración, tal y como exige la normativa contable que le es de aplicación.
