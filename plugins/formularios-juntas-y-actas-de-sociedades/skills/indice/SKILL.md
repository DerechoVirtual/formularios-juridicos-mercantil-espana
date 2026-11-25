---
name: indice
description: "Índice de los 171 formularios de Juntas, consejos y actas de sociedades de capital. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Juntas, consejos y actas de sociedades de capital: índice de formularios

> Plugin `formularios-juntas-y-actas-de-sociedades` · 171 formularios · normativa revisada el 25-11-2026.

## Qué es

Para la vida orgánica de las SL y SA: convocatorias de junta general, actas y listas de asistencia, certificaciones de acuerdos, representación y voto, sesiones y acuerdos del consejo de administración, y su elevación a público e inscripción.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Convocatoria de junta general ordinaria de una SL»
- «Acta de la junta universal que aprueba las cuentas»
- «Certificación de los acuerdos del consejo de administración»

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

### Cómo elegir

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-juntas-y-actas-de-sociedades:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado: el formulario que se rellena está en `../<skill>/assets/formulario.md` y la guía del tema es el `marco.md` de esta carpeta.

### Demandas, peticiones y solicitudes iniciales (1)

| Código | Formulario | Skill |
|---|---|---|
| MER-0310 | Demanda de convocatoria judicial de junta general ordinaria de sociedad anónima (art. 169.1 TRLSC) | `demanda-convocatoria-judicial-junta-general-ordinaria-mer-0310` |

### Contestaciones, oposiciones y alegaciones (1)

| Código | Formulario | Skill |
|---|---|---|
| MER-0117 | Escrito de oposición a la solicitud de acta notarial de junta formulada por la minoría | `escrito-oposicion-solicitud-acta-notarial-junta-mer-0117` |

### Contratos, pactos y cláusulas (3)

| Código | Formulario | Skill |
|---|---|---|
| MER-0012 | Acuerdo de desconvocatoria de una junta general de SL o SA | `acuerdo-desconvocatoria-junta-general-sl-sa-mer-0012` |
| MER-0081 | Acuerdo del consejo de administración de SA que convoca junta general y fija el orden del día | `acuerdo-consejo-administracion-sa-convoca-junta-mer-0081` |
| MER-0086 | Acuerdo del consejo de administración de formular las cuentas anuales | `acuerdo-consejo-administracion-formular-cuentas-anuales-mer-0086` |

### Estatutos, actas, certificaciones y escrituras (135)

| Código | Formulario | Skill |
|---|---|---|
| MER-0003 | Acta de disolución y liquidación de sociedad limitada o anónima unipersonal | `acta-disolucion-liquidacion-sociedad-limitada-anonima-mer-0003` |
| MER-0005 | Certificación de no aprobación de cuentas anuales para evitar el cierre registral de SL o SA | `certificacion-no-aprobacion-cuentas-anuales-evitar-mer-0005` |
| MER-0008 | Convocatoria de junta general de una SA exclusivamente telemática | `convocatoria-junta-general-sa-exclusivamente-telematica-mer-0008` |
| MER-0010 | Acta notarial de titularidad real de una SL o SA | `acta-notarial-titularidad-real-sl-sa-mer-0010` |
| MER-0011 | Acta de aportación de los socios a fondos propios sin aumento de capital en una SL | `acta-aportacion-socios-fondos-propios-sin-aumento-mer-0011` |
| MER-0014 | Certificación del acuerdo de crear una sucursal en el extranjero de una SA unipersonal | `certificacion-acuerdo-crear-sucursal-extranjero-sa-mer-0014` |
| MER-0015 | Acta de la decisión de crear una sucursal en el extranjero de una SA unipersonal | `acta-decision-crear-sucursal-extranjero-sa-unipersonal-mer-0015` |
| MER-0018 | Acta de junta general de SA que aprueba el balance final de liquidación y cesa a los liquidadores | `acta-junta-general-sa-aprueba-balance-final-mer-0018` |
| MER-0019 | Acta de junta de SL sobre dividendos a cuenta, reposición de pérdidas y reparto de reservas | `acta-junta-sl-sobre-dividendos-cuenta-reposicion-mer-0019` |
| MER-0021 | Acta de junta general extraordinaria y universal de SL que acuerda emitir obligaciones | `acta-junta-general-extraordinaria-universal-sl-acuerda-mer-0021` |
| MER-0023 | Acta notarial de una junta universal de SL | `acta-notarial-junta-universal-sl-mer-0023` |
| MER-0024 | Acta de junta de SL sobre cese y nombramiento de administradores o consejo de administración | `acta-junta-sl-sobre-cese-nombramiento-administradores-mer-0024` |
| MER-0025 | Acta de junta general de SL que aprueba las cuentas anuales y el reparto de beneficios | `acta-junta-general-sl-aprueba-cuentas-anuales-reparto-mer-0025` |
| MER-0026 | Acta de junta de SL que renueva el cargo de administradores o del consejo de administración | `acta-junta-sl-renueva-cargo-administradores-consejo-mer-0026` |
| MER-0027 | Acta de junta de SA sobre cese y nombramiento de administradores o consejo de administración | `acta-junta-sa-sobre-cese-nombramiento-administradores-mer-0027` |
| MER-0028 | Acta de junta de SL que acuerda modificar los estatutos sociales | `acta-junta-sl-acuerda-modificar-estatutos-sociales-mer-0028` |
| MER-0030 | Certificación del acuerdo de modificación de estatutos de una SL | `certificacion-acuerdo-modificacion-estatutos-sl-mer-0030` |
| MER-0031 | Acta de junta de SA que acuerda reducir el capital social | `acta-junta-sa-acuerda-reducir-capital-social-mer-0031` |
| MER-0033 | Acta de junta de SL que acuerda reducir el capital social | `acta-junta-sl-acuerda-reducir-capital-social-mer-0033` |
| MER-0034 | Certificación del acuerdo de reducción de capital de una SL | `certificacion-acuerdo-reduccion-capital-sl-mer-0034` |
| MER-0036 | Certificación del acuerdo de reducción de capital de una SA | `certificacion-acuerdo-reduccion-capital-sa-mer-0036` |
| MER-0037 | Acta de junta de SA que acuerda aumentar el capital social | `acta-junta-sa-acuerda-aumentar-capital-social-mer-0037` |
| MER-0038 | Acta de junta de SL que acuerda aumentar el capital social | `acta-junta-sl-acuerda-aumentar-capital-social-mer-0038` |
| MER-0040 | Certificación del acuerdo de aumento de capital de una SL | `certificacion-acuerdo-aumento-capital-sl-mer-0040` |
| MER-0045 | Acta de junta de SL que autoriza la venta de participaciones con conflicto de intereses | `acta-junta-sl-autoriza-venta-participaciones-conflicto-mer-0045` |
| MER-0054 | Anuncio de convocatoria de junta de SL para modificar los estatutos | `anuncio-convocatoria-junta-sl-modificar-estatutos-mer-0054` |
| MER-0062 | Convocatoria individual de junta de SL para aprobar las cuentas anuales | `convocatoria-individual-junta-sl-aprobar-cuentas-mer-0062` |
| MER-0064 | Convocatoria individual de junta de SL para aumentar capital sin derecho de preferencia | `convocatoria-individual-junta-sl-aumentar-capital-sin-mer-0064` |
| MER-0065 | Certificación de los administradores de SL de que ningún acreedor se ha opuesto | `certificacion-administradores-sl-ningun-acreedor-ha-mer-0065` |
| MER-0070 | Certificación de acuerdos del consejo de administración de una SL o SA | `certificacion-acuerdos-consejo-administracion-sl-sa-mer-0070` |
| MER-0071 | Acta de junta general que acuerda reactivar una sociedad disuelta | `acta-junta-general-acuerda-reactivar-sociedad-disuelta-mer-0071` |
| MER-0072 | Acta de junta de SL que acuerda la exclusión de un socio | `acta-junta-sl-acuerda-exclusion-socio-mer-0072` |
| MER-0073 | Acta de junta de SL que nombra administrador persona jurídica y suplentes y autoriza competencia | `acta-junta-sl-nombra-administrador-persona-juridica-mer-0073` |
| MER-0074 | Acta de junta de SL que acuerda la acción social de responsabilidad contra administradores | `acta-junta-sl-acuerda-accion-social-responsabilidad-mer-0074` |
| MER-0075 | Acta de junta de SL que acuerda la adquisición de participaciones propias | `acta-junta-sl-acuerda-adquisicion-participaciones-mer-0075` |
| MER-0076 | Acta de reunión del consejo de administración de una SL o SA | `acta-reunion-consejo-administracion-sl-sa-mer-0076` |
| MER-0077 | Certificación de los acuerdos de junta de SA adoptados ante notario | `certificacion-acuerdos-junta-sa-adoptados-ante-notario-mer-0077` |
| MER-0078 | Acta notarial de la firma de las acciones de una SA | `acta-notarial-firma-acciones-sa-mer-0078` |
| MER-0079 | Acta de junta de SL que aprueba las operaciones y el balance final de liquidación | `acta-junta-sl-aprueba-operaciones-balance-final-mer-0079` |
| MER-0080 | Acta notarial de la junta general de una SA | `acta-notarial-junta-general-sa-mer-0080` |
| MER-0083 | Certificación del libro registro de acciones nominativas de una SA | `certificacion-libro-registro-acciones-nominativas-sa-mer-0083` |
| MER-0084 | Convocatoria del consejo de administración por el presidente o los consejeros con acuse de recibo | `convocatoria-consejo-administracion-presidente-mer-0084` |
| MER-0085 | Certificación de pérdida del carácter unipersonal de una SL o SA | `certificacion-perdida-caracter-unipersonal-sl-sa-mer-0085` |
| MER-0091 | Poder privado de representación para asistir a la junta general de una SL o SA | `poder-privado-representacion-asistir-junta-general-sl-mer-0091` |
| MER-0109 | Certificación de unipersonalidad sobrevenida de una SL o SA | `certificacion-unipersonalidad-sobrevenida-sl-sa-mer-0109` |
| MER-0120 | Convocatoria de junta para modificar estatutos mediante anuncio y comunicación individual | `convocatoria-junta-modificar-estatutos-mediante-mer-0120` |
| MER-0122 | Acta de junta general de una sociedad unipersonal | `acta-junta-general-sociedad-unipersonal-mer-0122` |
| MER-0123 | Acta de junta de SA que aprueba las cuentas anuales, la gestión y la aplicación del resultado | `acta-junta-sa-aprueba-cuentas-anuales-gestion-mer-0123` |
| MER-0124 | Acta del consejo de SL que distribuye cargos, delega facultades y otorga poderes | `acta-consejo-sl-distribuye-cargos-delega-facultades-mer-0124` |
| MER-0125 | Certificación de cambio de socio único en una SL unipersonal | `certificacion-cambio-socio-unico-sl-unipersonal-mer-0125` |
| MER-0127 | Certificación bancaria del depósito de aportaciones dinerarias al capital social | `certificacion-bancaria-deposito-aportaciones-mer-0127` |
| MER-0128 | Anuncios de convocatoria de junta de SA para aprobar las cuentas anuales | `anuncios-convocatoria-junta-sa-aprobar-cuentas-anuales-mer-0128` |
| MER-0129 | Acta de junta extraordinaria y universal de SL que acuerda emitir obligaciones convertibles | `acta-junta-extraordinaria-universal-sl-acuerda-emitir-mer-0129` |
| MER-0130 | Acta de acuerdos del consejo de administración de SA adoptados por escrito y sin sesión | `acta-acuerdos-consejo-administracion-sa-adoptados-mer-0130` |
| MER-0134 | Acta de junta de SL o SA que designa al auditor de cuentas | `acta-junta-sl-sa-designa-auditor-cuentas-mer-0134` |
| MER-0136 | Anuncio de junta de SA para acordar reducción y aumento de capital simultáneos | `anuncio-junta-sa-acordar-reduccion-aumento-capital-mer-0136` |
| MER-0138 | Anuncio de junta de SA para aumentar capital excluyendo el derecho de suscripción preferente | `anuncio-junta-sa-aumentar-capital-excluyendo-derecho-mer-0138` |
| MER-0139 | Anuncio de convocatoria de junta general ordinaria de una sociedad cotizada | `anuncio-convocatoria-junta-general-ordinaria-sociedad-mer-0139` |
| MER-0142 | Convocatoria de junta extraordinaria para aprobar el balance final de liquidación | `convocatoria-junta-extraordinaria-aprobar-balance-mer-0142` |
| MER-0149 | Informe justificativo de la modificación de estatutos propuesta a la junta de una SA | `informe-justificativo-modificacion-estatutos-propuesta-mer-0149` |
| MER-0151 | Certificación del acuerdo del consejo de SA de cambiar el domicilio dentro del mismo municipio | `certificacion-acuerdo-consejo-sa-cambiar-domicilio-mer-0151` |
| MER-0166 | Acta del consejo de SA que cesa y nombra director general y revoca y otorga poderes | `acta-consejo-sa-cesa-nombra-director-general-revoca-mer-0166` |
| MER-0168 | Certificación de la delegación de facultades del consejo de administración de una SA | `certificacion-delegacion-facultades-consejo-mer-0168` |
| MER-0172 | Certificación de acuerdos del socio único de una sociedad anónima unipersonal | `certificacion-acuerdos-socio-unico-sociedad-anonima-mer-0172` |
| MER-0174 | Certificación del consejo sobre subsanación de errores en las cuentas anuales | `certificacion-consejo-sobre-subsanacion-errores-mer-0174` |
| MER-0177 | Convocatoria de junta de SA para ampliar capital con cargo a reservas | `convocatoria-junta-sa-ampliar-capital-cargo-reservas-mer-0177` |
| MER-0178 | Convocatoria de junta de SA para ampliar capital con aportaciones dinerarias | `convocatoria-junta-sa-ampliar-capital-aportaciones-mer-0178` |
| MER-0179 | Convocatoria de junta de SA para ampliar capital con aportaciones no dinerarias | `convocatoria-junta-sa-ampliar-capital-aportaciones-no-mer-0179` |
| MER-0180 | Convocatoria de junta de SA para ampliar capital por compensación de créditos | `convocatoria-junta-sa-ampliar-capital-compensacion-mer-0180` |
| MER-0181 | Convocatoria de junta de SA para ampliar capital elevando el valor nominal de las acciones | `convocatoria-junta-sa-ampliar-capital-elevando-valor-mer-0181` |
| MER-0182 | Convocatoria de junta de SA para ampliar capital mediante emisión de nuevas acciones | `convocatoria-junta-sa-ampliar-capital-mediante-emision-mer-0182` |
| MER-0187 | Certificación del acuerdo de creación o extinción de prestaciones accesorias en una SL | `certificacion-acuerdo-creacion-extincion-prestaciones-mer-0187` |
| MER-0188 | Certificación del acuerdo de modificar el régimen de transmisión de las participaciones de una SL | `certificacion-acuerdo-modificar-regimen-transmision-mer-0188` |
| MER-0189 | Acta de junta de una SL que modifica el régimen de transmisión de las participaciones | `acta-junta-sl-modifica-regimen-transmision-mer-0189` |
| MER-0190 | Acta de junta de una SL que crea o extingue prestaciones accesorias | `acta-junta-sl-crea-extingue-prestaciones-accesorias-mer-0190` |
| MER-0194 | Convocatoria de junta general de accionistas de una sociedad anónima | `convocatoria-junta-general-accionistas-sociedad-anonima-mer-0194` |
| MER-0197 | Certificación del acuerdo de aumento de capital de una sociedad anónima | `certificacion-acuerdo-aumento-capital-sociedad-anonima-mer-0197` |
| MER-0201 | Convocatoria de junta general ordinaria de una sociedad limitada | `convocatoria-junta-general-ordinaria-sociedad-limitada-mer-0201` |
| MER-0203 | Acta de decisiones del socio único de una SLU sobre cuentas anuales, dividendo a cuenta y auditor | `acta-decisiones-socio-unico-slu-sobre-cuentas-anuales-mer-0203` |
| MER-0204 | Certificación de la decisión del socio único de una SLU que aprueba las cuentas anuales | `certificacion-decision-socio-unico-slu-aprueba-cuentas-mer-0204` |
| MER-0206 | Acta del consejo de una SA sobre transmisión de acciones y propuesta de ampliación de capital | `acta-consejo-sa-sobre-transmision-acciones-propuesta-mer-0206` |
| MER-0207 | Acta de una reunión del consejo de administración de una SL o SA | `acta-reunion-consejo-administracion-sl-sa-mer-0207` |
| MER-0210 | Acta de junta de una SA que acuerda reducir y ampliar capital a la vez (operación acordeón) | `acta-junta-sa-acuerda-reducir-ampliar-capital-vez-mer-0210` |
| MER-0212 | Certificación del acuerdo de junta de una SA de reducir y ampliar capital a la vez (acordeón) | `certificacion-acuerdo-junta-sa-reducir-ampliar-capital-mer-0212` |
| MER-0213 | Acta del consejo de una SA que nombra un consejero por cooptación tras un fallecimiento | `acta-consejo-sa-nombra-consejero-cooptacion-tras-mer-0213` |
| MER-0214 | Acta de junta de una SA que crea o extingue anticipadamente prestaciones accesorias | `acta-junta-sa-crea-extingue-anticipadamente-mer-0214` |
| MER-0216 | Certificación de los acuerdos de la junta general extraordinaria de una sociedad anónima | `certificacion-acuerdos-junta-general-extraordinaria-mer-0216` |
| MER-0218 | Certificación del acuerdo de junta de nombrar auditor en una SL o SA | `certificacion-acuerdo-junta-nombrar-auditor-sl-sa-mer-0218` |
| MER-0219 | Anuncio de convocatoria de junta de una SA para cuentas anuales, cambio de objeto y de denominación | `anuncio-convocatoria-junta-sa-cuentas-anuales-cambio-mer-0219` |
| MER-0221 | Certificación del acta de junta universal de una SA que autoriza la venta de acciones | `certificacion-acta-junta-universal-sa-autoriza-venta-mer-0221` |
| MER-0225 | Acta del consejo de una SA que delega facultades y nombra consejero delegado o comisión ejecutiva | `acta-consejo-sa-delega-facultades-nombra-consejero-mer-0225` |
| MER-0233 | Acta de junta general de una SL, modelo general | `acta-junta-general-sl-modelo-general-mer-0233` |
| MER-0234 | Acta de junta general de una SL que acuerda la disolución | `acta-junta-general-sl-acuerda-disolucion-mer-0234` |
| MER-0235 | Escritura de requerimiento notarial de socios a los administradores de una SL para convocar junta | `escritura-requerimiento-notarial-socios-mer-0235` |
| MER-0239 | Certificación del acuerdo de junta de cese y nombramiento de administradores de una SL | `certificacion-acuerdo-junta-cese-nombramiento-mer-0239` |
| MER-0241 | Acta de junta de una SL que acuerda reducir y ampliar capital a la vez (operación acordeón) | `acta-junta-sl-acuerda-reducir-ampliar-capital-vez-mer-0241` |
| MER-0242 | Certificación del acuerdo de junta de una SL de reducir y ampliar capital a la vez (acordeón) | `certificacion-acuerdo-junta-sl-reducir-ampliar-capital-mer-0242` |
| MER-0243 | Acta de junta universal de una SL, modelo general | `acta-junta-universal-sl-modelo-general-mer-0243` |
| MER-0244 | Certificación del acuerdo de aprobación de las cuentas anuales de una SL | `certificacion-acuerdo-aprobacion-cuentas-anuales-sl-mer-0244` |
| MER-0245 | Certificación del acuerdo de junta de disolver una sociedad limitada | `certificacion-acuerdo-junta-disolver-sociedad-limitada-mer-0245` |
| MER-0246 | Certificación del acuerdo de junta de disolver y liquidar a la vez una sociedad limitada | `certificacion-acuerdo-junta-disolver-liquidar-vez-mer-0246` |
| MER-0248 | Acta de junta general de una SL que acuerda disolver y liquidar la sociedad a la vez | `acta-junta-general-sl-acuerda-disolver-liquidar-mer-0248` |
| MER-0249 | Certificación del acuerdo de junta que aprueba la liquidación de una sociedad limitada | `certificacion-acuerdo-junta-aprueba-liquidacion-mer-0249` |
| MER-0252 | Acta de junta general de una SL que aprueba la liquidación de la sociedad | `acta-junta-general-sl-aprueba-liquidacion-sociedad-mer-0252` |
| MER-0253 | Certificación del acuerdo de junta de reactivar una sociedad disuelta | `certificacion-acuerdo-junta-reactivar-sociedad-disuelta-mer-0253` |
| MER-0254 | Certificación del acuerdo de aprobación de las cuentas anuales de una sociedad anónima | `certificacion-acuerdo-aprobacion-cuentas-anuales-mer-0254` |
| MER-0263 | Certificación en extracto sobre la adquisición preferente en la venta de acciones nominativas | `certificacion-extracto-sobre-adquisicion-preferente-mer-0263` |
| MER-0266 | Certificación del órgano de administración que autoriza la transmisión de acciones nominativas | `certificacion-organo-administracion-autoriza-mer-0266` |
| MER-0269 | Certificación del administrador de una SL sobre la inscripción de un socio en el libro de socios | `certificacion-administrador-sl-sobre-inscripcion-socio-mer-0269` |
| MER-0273 | Certificación del órgano de administración que autoriza la transmisión de participaciones de una SL | `certificacion-organo-administracion-autoriza-mer-0273` |
| MER-0275 | Certificación del acuerdo de junta de una SL de crear una sucursal | `certificacion-acuerdo-junta-sl-crear-sucursal-mer-0275` |
| MER-0276 | Acta del consejo de administración de una SL que acuerda crear una sucursal | `acta-consejo-administracion-sl-acuerda-crear-sucursal-mer-0276` |
| MER-0277 | Escritura pública del acuerdo del consejo de administración de una SL de crear una sucursal | `escritura-publica-acuerdo-consejo-administracion-sl-mer-0277` |
| MER-0278 | Certificación del acuerdo del consejo de administración de una SL de crear una sucursal | `certificacion-acuerdo-consejo-administracion-sl-crear-mer-0278` |
| MER-0279 | Escritura pública del acuerdo de junta de una SL de crear una sucursal | `escritura-publica-acuerdo-junta-sl-crear-sucursal-mer-0279` |
| MER-0280 | Acta de junta de una SL que acuerda crear una sucursal | `acta-junta-sl-acuerda-crear-sucursal-mer-0280` |
| MER-0281 | Acta de la junta constituyente en la fundación sucesiva de una sociedad anónima | `acta-junta-constituyente-fundacion-sucesiva-sociedad-mer-0281` |
| MER-0284 | Acta de junta general universal ordinaria de una sociedad anónima | `acta-junta-general-universal-ordinaria-sociedad-anonima-mer-0284` |
| MER-0285 | Certificación de los acuerdos de la junta general ordinaria, universal o no, de una sociedad anónima | `certificacion-acuerdos-junta-general-ordinaria-mer-0285` |
| MER-0287 | Acta de junta general de una SA que acuerda emitir obligaciones convertibles o no convertibles | `acta-junta-general-sa-acuerda-emitir-obligaciones-mer-0287` |
| MER-0288 | Certificación del acuerdo de junta de una SA de crear una sucursal | `certificacion-acuerdo-junta-sa-crear-sucursal-mer-0288` |
| MER-0289 | Certificación del acuerdo de junta de cese y nombramiento de administradores de una sociedad anónima | `certificacion-acuerdo-junta-cese-nombramiento-mer-0289` |
| MER-0290 | Escritura pública del acuerdo de junta de una SA de crear una sucursal | `escritura-publica-acuerdo-junta-sa-crear-sucursal-mer-0290` |
| MER-0291 | Acta de junta general extraordinaria de una SA que acuerda la liquidación de la sociedad | `acta-junta-general-extraordinaria-sa-acuerda-mer-0291` |
| MER-0292 | Certificación del acuerdo de junta que aprueba la liquidación de una sociedad anónima | `certificacion-acuerdo-junta-aprueba-liquidacion-mer-0292` |
| MER-0293 | Acta de junta general extraordinaria de una SA que acuerda la disolución | `acta-junta-general-extraordinaria-sa-acuerda-disolucion-mer-0293` |
| MER-0294 | Certificación del acuerdo de junta de disolver una sociedad anónima | `certificacion-acuerdo-junta-disolver-sociedad-anonima-mer-0294` |
| MER-0295 | Certificación del acuerdo de junta de una SA de crear o extinguir prestaciones accesorias | `certificacion-acuerdo-junta-sa-crear-extinguir-mer-0295` |
| MER-0296 | Certificación del acuerdo del consejo de administración de una SA de crear una sucursal | `certificacion-acuerdo-consejo-administracion-sa-crear-mer-0296` |
| MER-0297 | Acta de junta de una SA que acuerda crear una sucursal | `acta-junta-sa-acuerda-crear-sucursal-mer-0297` |
| MER-0298 | Escritura pública del acuerdo del consejo de administración de una SA de crear una sucursal | `escritura-publica-acuerdo-consejo-administracion-sa-mer-0298` |
| MER-0299 | Acta del consejo de administración de una SA que acuerda crear una sucursal | `acta-consejo-administracion-sa-acuerda-crear-sucursal-mer-0299` |
| MER-0301 | Certificación del acuerdo de junta de disolver y liquidar a la vez una sociedad anónima | `certificacion-acuerdo-junta-disolver-liquidar-vez-mer-0301` |
| MER-0302 | Acta de junta general extraordinaria de una SA que acuerda disolver y liquidar la sociedad a la vez | `acta-junta-general-extraordinaria-sa-acuerda-disolver-mer-0302` |
| MER-0306 | Convocatoria de la junta general constitutiva de una sociedad | `convocatoria-junta-general-constitutiva-sociedad-mer-0306` |

### Comunicaciones, requerimientos y cartas (23)

| Código | Formulario | Skill |
|---|---|---|
| MER-0055 | Solicitud del socio de examinar la documentación de las cuentas anuales antes de la junta de SL | `solicitud-socio-examinar-documentacion-cuentas-anuales-mer-0055` |
| MER-0056 | Solicitud de certificación registral para el traslado de domicilio de una SL | `solicitud-certificacion-registral-traslado-domicilio-sl-mer-0056` |
| MER-0057 | Solicitud del socio de convocar junta de SL para acordar la disolución | `solicitud-socio-convocar-junta-sl-acordar-disolucion-mer-0057` |
| MER-0092 | Solicitud escrita de informes o aclaraciones sobre el orden del día antes de la junta | `solicitud-escrita-informes-aclaraciones-sobre-orden-mer-0092` |
| MER-0112 | Solicitud de duplicado o renovación de la certificación de denominación social | `solicitud-duplicado-renovacion-certificacion-mer-0112` |
| MER-0113 | Solicitud de certificación negativa de denominación social al Registro Mercantil Central | `solicitud-certificacion-negativa-denominacion-social-mer-0113` |
| MER-0114 | Solicitud de certificación registral del nombramiento de administradores | `solicitud-certificacion-registral-nombramiento-mer-0114` |
| MER-0115 | Solicitud del accionista de certificación del libro registro de acciones nominativas | `solicitud-accionista-certificacion-libro-registro-mer-0115` |
| MER-0133 | Solicitud al letrado de la Administración de Justicia de convocatoria de junta extraordinaria de SA | `solicitud-letrado-administracion-justicia-convocatoria-mer-0133` |
| MER-0141 | Carta circular para votación escrita y sin sesión del consejo de administración de una SA | `carta-circular-votacion-escrita-sin-sesion-consejo-mer-0141` |
| MER-0164 | Solicitud pública de representación para la junta general de una SA | `solicitud-publica-representacion-junta-general-sa-mer-0164` |
| MER-0165 | Solicitud de complemento de la convocatoria de la junta de una SA | `solicitud-complemento-convocatoria-junta-sa-mer-0165` |
| MER-0176 | Carta de convocatoria de junta de SA para reducir el capital social | `carta-convocatoria-junta-sa-reducir-capital-social-mer-0176` |
| MER-0191 | Carta de representación de un socio de SL para asistir a la junta general | `carta-representacion-socio-sl-asistir-junta-general-mer-0191` |
| MER-0200 | Solicitud del accionista al consejo de la documentación de las cuentas anuales antes de la junta | `solicitud-accionista-consejo-documentacion-cuentas-mer-0200` |
| MER-0258 | Requerimiento notarial a los administradores de una SA para que convoquen junta extraordinaria | `requerimiento-notarial-administradores-sa-convoquen-mer-0258` |
| MER-0261 | Requerimiento a los administradores de una SA para que un notario levante acta de la junta general | `requerimiento-administradores-sa-notario-levante-acta-mer-0261` |
| MER-0267 | Solicitud de socios minoritarios de una SA para convocar junta general ordinaria o extraordinaria | `solicitud-socios-minoritarios-sa-convocar-junta-mer-0267` |
| MER-0270 | Solicitud de un socio de SL de certificación del libro registro de socios | `solicitud-socio-sl-certificacion-libro-registro-socios-mer-0270` |
| MER-0271 | Solicitud de socios de una SL para convocar junta que apruebe las cuentas anuales | `solicitud-socios-sl-convocar-junta-apruebe-cuentas-mer-0271` |
| MER-0274 | Requerimiento a los administradores de una SL para que un notario levante acta de la junta general | `requerimiento-administradores-sl-notario-levante-acta-mer-0274` |
| MER-0303 | Carta de socios a los administradores solicitando convocar la junta general de una SL o SA | `carta-socios-administradores-solicitando-convocar-mer-0303` |
| MER-0309 | Solicitud de convocatoria de junta extraordinaria de SL por socios con el 5 por ciento del capital | `solicitud-convocatoria-junta-extraordinaria-sl-socios-mer-0309` |

### Escritos de trámite y otros (8)

| Código | Formulario | Skill |
|---|---|---|
| MER-0052 | Anexo al acta de junta de SA sobre quórum y suspensión del voto de las acciones propias | `anexo-acta-junta-sa-sobre-quorum-suspension-voto-mer-0052` |
| MER-0066 | Lista de asistentes a la junta general de una SL | `lista-asistentes-junta-general-sl-mer-0066` |
| MER-0087 | Delegación de voto de un consejero en otro para asistir al consejo de administración | `delegacion-voto-consejero-otro-asistir-consejo-mer-0087` |
| MER-0104 | Respuesta de los administradores que envía o deniega información sobre el orden del día de la junta | `respuesta-administradores-envia-deniega-informacion-mer-0104` |
| MER-0111 | Diligencia de aprobación diferida del acta de la junta general | `diligencia-aprobacion-diferida-acta-junta-general-mer-0111` |
| MER-0135 | Votación escrita y sin sesión del consejo de SA sobre aceptación, nombramientos y reparto de cargos | `votacion-escrita-sin-sesion-consejo-sa-sobre-mer-0135` |
| MER-0217 | Escrito de autorización para que otra persona represente al socio en la junta general de una SL o SA | `escrito-autorizacion-otra-persona-represente-socio-mer-0217` |
| MER-0286 | Lista de asistentes a la junta general de accionistas de una sociedad anónima | `lista-asistentes-junta-general-accionistas-sociedad-mer-0286` |
