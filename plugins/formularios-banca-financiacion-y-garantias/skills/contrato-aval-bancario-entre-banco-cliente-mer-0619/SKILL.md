---
name: contrato-aval-bancario-entre-banco-cliente-mer-0619
description: "Contrato de aval bancario entre banco y cliente. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de aval bancario entre banco y cliente

> Formulario **MER-0619** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de aval bancario entre banco y cliente» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de aval bancario entre banco y cliente” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:contrato-aval-bancario-entre-banco-cliente-mer-0619`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (9 veces)
- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] FECHA (6 veces)
- [ ] NÚMERO (4 veces)
- [ ] DOMICILIO (3 veces)
- [ ] NIF (3 veces)
- [ ] PROVINCIA (3 veces)
- [ ] CALLE (2 veces)
- [ ] FOLIO (2 veces)
- [ ] NOMBRE DEL BENEFICIARIO (2 veces)
- [ ] TOMO (2 veces)
- [ ] CARGO
- [ ] COLEGIO
- [ ] DENOMINACIÓN SOCIAL
- [ ] ENTIDAD BANCARIA
- [ ] HOJA
- [ ] IMPORTE
- [ ] INSCRIPCIÓN
- [ ] LIBRO
- [ ] SECCIÓN
- [ ] TIPO DE INTERÉS
- [ ] ÓRGANO
- [ ] ÓRGANO O PERSONA

## Normas que cita el formulario

- art. 1851 Código Civil
- art. 20.18.f Ley 37/1992

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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD)»: La LO 15/1999 y su Reglamento (RD 1720/2007) fueron sustituidos por el Reglamento (UE) 2016/679 (RGPD) y la LO 3/2018, de 5 de diciembre (LOPDGDD). Fuente: LO 3/2018, disposición derogatoria única.

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

Operación de garantía por la que el avalista (banco) se compromete a responder del cumplimiento de una obligación del avalado (cliente) ante un tercero (beneficiario), en caso de que el avalado no lo haga.

En [LOCALIDAD], a fecha de [FECHA]

Y ante [ÓRGANO], Notario del Ilustre Colegio de [COLEGIO]

Comparecen:

De una parte [DENOMINACIÓN SOCIAL], como AVALISTA/FIADOR (jurídica)

D/Dª [NOMBRE Y APELLIDOS] (detallar nombre y apellidos), en nombre y representación de la entidad bancaria [ENTIDAD BANCARIA] (detallar) situada [LOCALIDAD] (detallar localidad), y con CIF número [NIF] (detallar), constituida por tiempo indefinido mediante escritura otorgada ante notario de [LOCALIDAD] (detallar localidad), D/Dª [NOMBRE Y APELLIDOS] (detallar nombre y apellidos) [FECHA] (detallar fecha) e inscrita en el Registro mercantil de [PROVINCIA] (detallar provincia), en el tomo [TOMO] (detallar), folio [FOLIO] (detallar), sección [SECCIÓN] (detallar), hoja [HOJA] (detallar), inscripción [INSCRIPCIÓN] (detallar), en su calidad de:

— Cargo social [CARGO] (detallar administrador único, solidario, consejero delegado) de la reseñada sociedad, cargo para el que fue nombrado y asegura vigente en escritura pública otorgada el [FECHA] (detallar fecha), ante notario de [LOCALIDAD] (detallar localidad), D/Dª [NOMBRE Y APELLIDOS] (detallar nombre y apellidos), con el número [NÚMERO] (detallar) de su protocolo, e inscrita en el Registro mercantil de la provincia [PROVINCIA] (detallar), en el tomo y hoja arriba indicados, con poderes suficientes para obligarle en este acto, según resulta de la verificación de la representación de la parte inferior de este documento.

— Apoderado de la señalada sociedad, según escritura de poder otorgada a su favor en [FECHA] (detallar fecha), ante notario de de [LOCALIDAD] (detallar localidad), D/Dª [NOMBRE Y APELLIDOS] (detallar nombre y apellidos) con el número [NÚMERO] (detallar) de su protocolo, e inscrita en el Registro mercantil de la provincia [PROVINCIA] (detallar), en el tomo y hoja arriba indicados, con poderes suficientes para obligarle en este acto, según resulta de la verificación de la representación de la parte inferior de este documento.

De otra parte, como AVALADO,

(persona física: D/Dª [NOMBRE Y APELLIDOS] mayor de edad, estado civil (especificar en su caso régimen económico matrimonial en caso de que el estado civil sea casado)

(Persona jurídica: constituida en escritura pública otorgada el día [FECHA] ante Notario de [LOCALIDAD] D/Dª [NOMBRE Y APELLIDOS] e inscrita en el Registro Mercantil de [LOCALIDAD] Libro [LIBRO] Tomo [TOMO] Folio [FOLIO] domiciliada en [DOMICILIO] calle [CALLE] núm [NÚMERO] y con CIF núm [NIF] representada por [ÓRGANO O PERSONA], mayor de edad, con domicilio en [LOCALIDAD] c/ [CALLE] núm [NÚMERO] con DNI/NIF núm [NIF] cuyas facultades derivan del poder otorgando por el notario D/Dª [NOMBRE Y APELLIDOS], debidamente inscrito, que es declarado vigente y sin modificación alguna).

Cláusulas

1. Objeto: por el presente contrato, el AVALISTA/FIADOR se obliga a garantizar el cumplimiento de la obligaciones que, que con fecha [FECHA] (detallar), el AVALADO, se comprometió a realizar a [NOMBRE DEL BENEFICIARIO].

2. Alcance y límite de la garantía: el importe garantizado será [IMPORTE] (detallar)

3. Garantías. Este aval se pacta con carácter solidario y durará mientras esté vigente la última de las obligaciones a las que el AVALADO se ha comprometido con [NOMBRE DEL BENEFICIARIO] (detallar), incluyendo cualquier prórroga que las partes puedan pactar, sin necesidad en este último caso de ratificación alguna por parte de los fiadores, renunciando en este acto los fiadores a las consecuencias previstas en el artículo 1851 del Código Civil.

4. Intereses. Las cantidades que haya de abonar el AVALADO y que resulten impagadas por el AVALISTA/FIADOR una vez que haya vencido la obligación de pago, generarán a favor del primero un tipo de interés diario igual al tipo [TIPO DE INTERÉS] (detallar %) y que será objeto de liquidación el día de la cuenta especial de impagados. El AVALADO queda autorizado para cargar en una cuenta especial que se abrirá al efecto a nombre del AVALISTA/FIADOR quedando este último obligado desde este momento al reintegro de la misma.

5. Duración del contrato. El presente contrato mantendrá su vigencia en tanto en cuanto no se culmine la obligación principal.

6. Mantenimiento del contrato. Si cualquiera de los pactos de este contrato fuera declarado inválido, ya sea de modo parcial o total, el resto del contrato mantendrá su vigencia y eficacia.

7. Gastos e impuestos. Todos los gastos, tributos, honorarios derivados de la formalización de la póliza serán de cuenta del AVALADO

8. Intervención de notario. Este contrato ha sido formalizado con la intervención de notario a todos los efectos previstos.

9. Notificaciones. A efectos de requerimiento, notificaciones y citaciones de cualquier clase, se especifican como domicilios

AVALISTA/FIADOR [DOMICILIO] (detallar)

AVALADO [DOMICILIO] (detallar)

10. Fiscalidad. Las partes manifiestan de común acuerdo que el presente contrato se encuentra sujeto al impuesto del Valor Añadido, pero exenta por tratarse de una de las operaciones financieras contempladas en el artículo 20.18.f) de la Ley 37/1992, de 28 de diciembre.

11. Tribunal competente. Para solucionar cualquier cuestión litigiosa que pueda derivarse del presente contrato, las partes, con renuncia al fuero aplicable, se someten voluntariamente a la jurisdicción de los tribunales de [LOCALIDAD] (detallar ciudad).

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Las partes dan su conformidad:

EL AVALISTA/FIADOR EL AVALADO
