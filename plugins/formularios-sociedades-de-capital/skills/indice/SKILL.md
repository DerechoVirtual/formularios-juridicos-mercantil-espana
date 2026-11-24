---
name: indice
description: "Índice de los 310 formularios de Sociedades de capital: juntas, administradores, capital y cuentas. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Sociedades de capital: juntas, administradores, capital y cuentas: índice de formularios

> Plugin `formularios-sociedades-de-capital` · 310 formularios · normativa revisada el 24-11-2026.

## Qué es

Para el día a día societario de las SL y SA: convocatorias y actas de junta, certificaciones de acuerdos, nombramiento y cese de administradores, consejos de administración, aumentos y reducciones de capital, transmisión de participaciones y acciones, cuentas anuales, auditor, disolución y liquidación, y los escritos al Registro Mercantil.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Convocatoria de junta general de una SL para aprobar las cuentas»
- «Certificación del acuerdo de aumento de capital de una SA»
- «Renuncia de un administrador y su comunicación al Registro Mercantil»

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

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-sociedades-de-capital:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado: el formulario está al final de ese fichero y la guía del tema es el `marco.md` de esta carpeta.

### Demandas, peticiones y solicitudes iniciales (2)

| Código | Formulario | Skill |
|---|---|---|
| MER-0146 | Solicitud de nombramiento de auditor al Registro Mercantil para verificar las cuentas anuales | `solicitud-nombramiento-auditor-registro-mercantil-mer-0146` |
| MER-0310 | Demanda de convocatoria judicial de junta general ordinaria de sociedad anónima (art. 169.1 TRLSC) | `demanda-convocatoria-judicial-junta-general-ordinaria-mer-0310` |

### Contestaciones, oposiciones y alegaciones (4)

| Código | Formulario | Skill |
|---|---|---|
| MER-0090 | Escrito de oposición del acreedor social a la reducción de capital de una SA | `escrito-oposicion-acreedor-social-reduccion-capital-sa-mer-0090` |
| MER-0107 | Escrito de oposición a la rectificación del libro registro de acciones nominativas | `escrito-oposicion-rectificacion-libro-registro-mer-0107` |
| MER-0117 | Escrito de oposición a la solicitud de acta notarial de junta formulada por la minoría | `escrito-oposicion-solicitud-acta-notarial-junta-mer-0117` |
| MER-0171 | Escrito de oposición al nombramiento de auditor por el Registro Mercantil | `escrito-oposicion-nombramiento-auditor-registro-mer-0171` |

### Contratos, pactos y cláusulas (13)

| Código | Formulario | Skill |
|---|---|---|
| MER-0009 | Pacto de socios (modelo) | `pacto-socios-modelo-mer-0009` |
| MER-0012 | Acuerdo de desconvocatoria de una junta general de SL o SA | `acuerdo-desconvocatoria-junta-general-sl-sa-mer-0012` |
| MER-0013 | Contrato de compraventa de acciones o participaciones sociales (SPA) | `contrato-compraventa-acciones-participaciones-sociales-mer-0013` |
| MER-0017 | Pacto parasocial para la constitución de una sociedad | `pacto-parasocial-constitucion-sociedad-mer-0017` |
| MER-0042 | Contrato de inversión entre la sociedad y business angels | `contrato-inversion-entre-sociedad-business-angels-mer-0042` |
| MER-0043 | Carta de intenciones de inversión con business angels | `carta-intenciones-inversion-business-angels-mer-0043` |
| MER-0044 | Acuerdo de gestión entre red de business angels, inversor y emprendedor | `acuerdo-gestion-entre-red-business-angels-inversor-mer-0044` |
| MER-0046 | Compraventa de acciones de una sociedad (contrato) | `compraventa-acciones-sociedad-contrato-mer-0046` |
| MER-0050 | Contrato con el consejero delegado de una SL (art. 249.3 LSC) | `contrato-consejero-delegado-sl-art-249-3-lsc-mer-0050` |
| MER-0081 | Acuerdo del consejo de administración de SA que convoca junta general y fija el orden del día | `acuerdo-consejo-administracion-sa-convoca-junta-mer-0081` |
| MER-0086 | Acuerdo del consejo de administración de formular las cuentas anuales | `acuerdo-consejo-administracion-formular-cuentas-anuales-mer-0086` |
| MER-0145 | Compraventa de acciones nominativas entre personas físicas (contrato) | `compraventa-acciones-nominativas-entre-personas-mer-0145` |
| MER-0199 | Contrato de venta de participaciones de una sociedad limitada | `contrato-venta-participaciones-sociedad-limitada-mer-0199` |

### Estatutos, actas, certificaciones y escrituras (193)

| Código | Formulario | Skill |
|---|---|---|
| MER-0003 | Acta de disolución y liquidación de sociedad limitada o anónima unipersonal | `acta-disolucion-liquidacion-sociedad-limitada-anonima-mer-0003` |
| MER-0004 | Estatutos sociales de una SPAC | `estatutos-sociales-spac-mer-0004` |
| MER-0005 | Certificación de no aprobación de cuentas anuales para evitar el cierre registral de SL o SA | `certificacion-no-aprobacion-cuentas-anuales-evitar-mer-0005` |
| MER-0008 | Convocatoria de junta general de una SA exclusivamente telemática | `convocatoria-junta-general-sa-exclusivamente-telematica-mer-0008` |
| MER-0010 | Acta notarial de titularidad real de una SL o SA | `acta-notarial-titularidad-real-sl-sa-mer-0010` |
| MER-0011 | Acta de aportación de los socios a fondos propios sin aumento de capital en una SL | `acta-aportacion-socios-fondos-propios-sin-aumento-mer-0011` |
| MER-0014 | Certificación del acuerdo de crear una sucursal en el extranjero de una SA unipersonal | `certificacion-acuerdo-crear-sucursal-extranjero-sa-mer-0014` |
| MER-0015 | Acta de la decisión de crear una sucursal en el extranjero de una SA unipersonal | `acta-decision-crear-sucursal-extranjero-sa-unipersonal-mer-0015` |
| MER-0016 | Estatutos sociales de una sociedad limitada unipersonal | `estatutos-sociales-sociedad-limitada-unipersonal-mer-0016` |
| MER-0018 | Acta de junta general de SA que aprueba el balance final de liquidación y cesa a los liquidadores | `acta-junta-general-sa-aprueba-balance-final-mer-0018` |
| MER-0019 | Acta de junta de SL sobre dividendos a cuenta, reposición de pérdidas y reparto de reservas | `acta-junta-sl-sobre-dividendos-cuenta-reposicion-mer-0019` |
| MER-0021 | Acta de junta general extraordinaria y universal de SL que acuerda emitir obligaciones | `acta-junta-general-extraordinaria-universal-sl-acuerda-mer-0021` |
| MER-0023 | Acta notarial de una junta universal de SL | `acta-notarial-junta-universal-sl-mer-0023` |
| MER-0024 | Acta de junta de SL sobre cese y nombramiento de administradores o consejo de administración | `acta-junta-sl-sobre-cese-nombramiento-administradores-mer-0024` |
| MER-0025 | Acta de junta general de SL que aprueba las cuentas anuales y el reparto de beneficios | `acta-junta-general-sl-aprueba-cuentas-anuales-reparto-mer-0025` |
| MER-0026 | Acta de junta de SL que renueva el cargo de administradores o del consejo de administración | `acta-junta-sl-renueva-cargo-administradores-consejo-mer-0026` |
| MER-0027 | Acta de junta de SA sobre cese y nombramiento de administradores o consejo de administración | `acta-junta-sa-sobre-cese-nombramiento-administradores-mer-0027` |
| MER-0028 | Acta de junta de SL que acuerda modificar los estatutos sociales | `acta-junta-sl-acuerda-modificar-estatutos-sociales-mer-0028` |
| MER-0029 | Escritura pública de modificación de estatutos de una SL | `escritura-publica-modificacion-estatutos-sl-mer-0029` |
| MER-0030 | Certificación del acuerdo de modificación de estatutos de una SL | `certificacion-acuerdo-modificacion-estatutos-sl-mer-0030` |
| MER-0031 | Acta de junta de SA que acuerda reducir el capital social | `acta-junta-sa-acuerda-reducir-capital-social-mer-0031` |
| MER-0032 | Escritura pública de reducción del capital de una SA | `escritura-publica-reduccion-capital-sa-mer-0032` |
| MER-0033 | Acta de junta de SL que acuerda reducir el capital social | `acta-junta-sl-acuerda-reducir-capital-social-mer-0033` |
| MER-0034 | Certificación del acuerdo de reducción de capital de una SL | `certificacion-acuerdo-reduccion-capital-sl-mer-0034` |
| MER-0035 | Escritura pública de reducción del capital de una SL | `escritura-publica-reduccion-capital-sl-mer-0035` |
| MER-0036 | Certificación del acuerdo de reducción de capital de una SA | `certificacion-acuerdo-reduccion-capital-sa-mer-0036` |
| MER-0037 | Acta de junta de SA que acuerda aumentar el capital social | `acta-junta-sa-acuerda-aumentar-capital-social-mer-0037` |
| MER-0038 | Acta de junta de SL que acuerda aumentar el capital social | `acta-junta-sl-acuerda-aumentar-capital-social-mer-0038` |
| MER-0039 | Escritura pública de aumento de capital de una SL | `escritura-publica-aumento-capital-sl-mer-0039` |
| MER-0040 | Certificación del acuerdo de aumento de capital de una SL | `certificacion-acuerdo-aumento-capital-sl-mer-0040` |
| MER-0041 | Escritura pública de aumento de capital de una SA | `escritura-publica-aumento-capital-sa-mer-0041` |
| MER-0045 | Acta de junta de SL que autoriza la venta de participaciones con conflicto de intereses | `acta-junta-sl-autoriza-venta-participaciones-conflicto-mer-0045` |
| MER-0051 | Poder notarial para constituir una sociedad limitada | `poder-notarial-constituir-sociedad-limitada-mer-0051` |
| MER-0054 | Anuncio de convocatoria de junta de SL para modificar los estatutos | `anuncio-convocatoria-junta-sl-modificar-estatutos-mer-0054` |
| MER-0059 | Escritura pública de renuncia del administrador de una SL o SA | `escritura-publica-renuncia-administrador-sl-sa-mer-0059` |
| MER-0062 | Convocatoria individual de junta de SL para aprobar las cuentas anuales | `convocatoria-individual-junta-sl-aprobar-cuentas-mer-0062` |
| MER-0064 | Convocatoria individual de junta de SL para aumentar capital sin derecho de preferencia | `convocatoria-individual-junta-sl-aumentar-capital-sin-mer-0064` |
| MER-0065 | Certificación de los administradores de SL de que ningún acreedor se ha opuesto | `certificacion-administradores-sl-ningun-acreedor-ha-mer-0065` |
| MER-0068 | Anuncio de la reducción de capital de una SL para que los acreedores ejerzan su derecho de oposición | `anuncio-reduccion-capital-sl-acreedores-ejerzan-mer-0068` |
| MER-0069 | Anuncio en el BORME de un acuerdo de SL que da derecho de separación | `anuncio-borme-acuerdo-sl-da-derecho-separacion-mer-0069` |
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
| MER-0088 | Anuncio en prensa del acuerdo de reducción del capital de una SA | `anuncio-prensa-acuerdo-reduccion-capital-sa-mer-0088` |
| MER-0091 | Poder privado de representación para asistir a la junta general de una SL o SA | `poder-privado-representacion-asistir-junta-general-sl-mer-0091` |
| MER-0095 | Anuncio de oferta de nuevas participaciones de SL para el ejercicio del derecho de preferencia | `anuncio-oferta-nuevas-participaciones-sl-ejercicio-mer-0095` |
| MER-0108 | Estatutos sociales simplificados de una sociedad anónima | `estatutos-sociales-simplificados-sociedad-anonima-mer-0108` |
| MER-0109 | Certificación de unipersonalidad sobrevenida de una SL o SA | `certificacion-unipersonalidad-sobrevenida-sl-sa-mer-0109` |
| MER-0119 | Informe de los administradores de una SA sobre la propuesta de modificación de estatutos | `informe-administradores-sa-sobre-propuesta-mer-0119` |
| MER-0120 | Convocatoria de junta para modificar estatutos mediante anuncio y comunicación individual | `convocatoria-junta-modificar-estatutos-mediante-mer-0120` |
| MER-0121 | Anuncio en el BORME de la reclamación de desembolsos pendientes a los accionistas | `anuncio-borme-reclamacion-desembolsos-pendientes-mer-0121` |
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
| MER-0154 | Informe especial sobre créditos a compensar en un aumento de capital de SA | `informe-especial-sobre-creditos-compensar-aumento-mer-0154` |
| MER-0155 | Anuncio del acuerdo de reducción del capital de una SA | `anuncio-acuerdo-reduccion-capital-sa-mer-0155` |
| MER-0158 | Anuncio de reducción y aumento simultáneo de capital de SA con derecho de suscripción | `anuncio-reduccion-aumento-simultaneo-capital-sa-mer-0158` |
| MER-0160 | Informe de los administradores de SA sobre aportaciones no dinerarias en un aumento de capital | `informe-administradores-sa-sobre-aportaciones-no-mer-0160` |
| MER-0161 | Informe especial sobre la exclusión del derecho de suscripción preferente en aumento de capital | `informe-especial-sobre-exclusion-derecho-suscripcion-mer-0161` |
| MER-0162 | Anuncio de oferta de retirada de acciones de asignación gratuita en la ampliación de capital de SA | `anuncio-oferta-retirada-acciones-asignacion-gratuita-mer-0162` |
| MER-0166 | Acta del consejo de SA que cesa y nombra director general y revoca y otorga poderes | `acta-consejo-sa-cesa-nombra-director-general-revoca-mer-0166` |
| MER-0167 | Informe especial del auditor sobre las reservas usadas en la ampliación de capital de una SA | `informe-especial-auditor-sobre-reservas-usadas-mer-0167` |
| MER-0168 | Certificación de la delegación de facultades del consejo de administración de una SA | `certificacion-delegacion-facultades-consejo-mer-0168` |
| MER-0172 | Certificación de acuerdos del socio único de una sociedad anónima unipersonal | `certificacion-acuerdos-socio-unico-sociedad-anonima-mer-0172` |
| MER-0174 | Certificación del consejo sobre subsanación de errores en las cuentas anuales | `certificacion-consejo-sobre-subsanacion-errores-mer-0174` |
| MER-0177 | Convocatoria de junta de SA para ampliar capital con cargo a reservas | `convocatoria-junta-sa-ampliar-capital-cargo-reservas-mer-0177` |
| MER-0178 | Convocatoria de junta de SA para ampliar capital con aportaciones dinerarias | `convocatoria-junta-sa-ampliar-capital-aportaciones-mer-0178` |
| MER-0179 | Convocatoria de junta de SA para ampliar capital con aportaciones no dinerarias | `convocatoria-junta-sa-ampliar-capital-aportaciones-no-mer-0179` |
| MER-0180 | Convocatoria de junta de SA para ampliar capital por compensación de créditos | `convocatoria-junta-sa-ampliar-capital-compensacion-mer-0180` |
| MER-0181 | Convocatoria de junta de SA para ampliar capital elevando el valor nominal de las acciones | `convocatoria-junta-sa-ampliar-capital-elevando-valor-mer-0181` |
| MER-0182 | Convocatoria de junta de SA para ampliar capital mediante emisión de nuevas acciones | `convocatoria-junta-sa-ampliar-capital-mediante-emision-mer-0182` |
| MER-0183 | Escritura de constitución de una sociedad anónima deportiva | `escritura-constitucion-sociedad-anonima-deportiva-mer-0183` |
| MER-0184 | Estatutos sociales de una sociedad anónima deportiva | `estatutos-sociales-sociedad-anonima-deportiva-mer-0184` |
| MER-0185 | Escritura pública de reactivación de una sociedad de capital disuelta | `escritura-publica-reactivacion-sociedad-capital-mer-0185` |
| MER-0186 | Escritura pública de creación o extinción de prestaciones accesorias en una SL | `escritura-publica-creacion-extincion-prestaciones-mer-0186` |
| MER-0187 | Certificación del acuerdo de creación o extinción de prestaciones accesorias en una SL | `certificacion-acuerdo-creacion-extincion-prestaciones-mer-0187` |
| MER-0188 | Certificación del acuerdo de modificar el régimen de transmisión de las participaciones de una SL | `certificacion-acuerdo-modificar-regimen-transmision-mer-0188` |
| MER-0189 | Acta de junta de una SL que modifica el régimen de transmisión de las participaciones | `acta-junta-sl-modifica-regimen-transmision-mer-0189` |
| MER-0190 | Acta de junta de una SL que crea o extingue prestaciones accesorias | `acta-junta-sl-crea-extingue-prestaciones-accesorias-mer-0190` |
| MER-0192 | Estatutos sociales de una sociedad anónima unipersonal | `estatutos-sociales-sociedad-anonima-unipersonal-mer-0192` |
| MER-0193 | Escritura pública del acuerdo de disolución de una sociedad anónima | `escritura-publica-acuerdo-disolucion-sociedad-anonima-mer-0193` |
| MER-0194 | Convocatoria de junta general de accionistas de una sociedad anónima | `convocatoria-junta-general-accionistas-sociedad-anonima-mer-0194` |
| MER-0195 | Escritura pública de compraventa de acciones al portador de una SA | `escritura-publica-compraventa-acciones-portador-sa-mer-0195` |
| MER-0196 | Escritura pública de compraventa de acciones nominativas de una SA | `escritura-publica-compraventa-acciones-nominativas-sa-mer-0196` |
| MER-0197 | Certificación del acuerdo de aumento de capital de una sociedad anónima | `certificacion-acuerdo-aumento-capital-sociedad-anonima-mer-0197` |
| MER-0198 | Escritura notarial de otorgamiento de poder | `escritura-notarial-otorgamiento-poder-mer-0198` |
| MER-0201 | Convocatoria de junta general ordinaria de una sociedad limitada | `convocatoria-junta-general-ordinaria-sociedad-limitada-mer-0201` |
| MER-0203 | Acta de decisiones del socio único de una SLU sobre cuentas anuales, dividendo a cuenta y auditor | `acta-decisiones-socio-unico-slu-sobre-cuentas-anuales-mer-0203` |
| MER-0204 | Certificación de la decisión del socio único de una SLU que aprueba las cuentas anuales | `certificacion-decision-socio-unico-slu-aprueba-cuentas-mer-0204` |
| MER-0206 | Acta del consejo de una SA sobre transmisión de acciones y propuesta de ampliación de capital | `acta-consejo-sa-sobre-transmision-acciones-propuesta-mer-0206` |
| MER-0207 | Acta de una reunión del consejo de administración de una SL o SA | `acta-reunion-consejo-administracion-sl-sa-mer-0207` |
| MER-0208 | Escritura pública de liquidación de una sociedad anónima | `escritura-publica-liquidacion-sociedad-anonima-mer-0208` |
| MER-0209 | Escritura pública de cese y nombramiento de administradores de una sociedad anónima | `escritura-publica-cese-nombramiento-administradores-mer-0209` |
| MER-0210 | Acta de junta de una SA que acuerda reducir y ampliar capital a la vez (operación acordeón) | `acta-junta-sa-acuerda-reducir-ampliar-capital-vez-mer-0210` |
| MER-0211 | Escritura pública de reducción y ampliación simultánea de capital de una SA (operación acordeón) | `escritura-publica-reduccion-ampliacion-simultanea-mer-0211` |
| MER-0212 | Certificación del acuerdo de junta de una SA de reducir y ampliar capital a la vez (acordeón) | `certificacion-acuerdo-junta-sa-reducir-ampliar-capital-mer-0212` |
| MER-0213 | Acta del consejo de una SA que nombra un consejero por cooptación tras un fallecimiento | `acta-consejo-sa-nombra-consejero-cooptacion-tras-mer-0213` |
| MER-0214 | Acta de junta de una SA que crea o extingue anticipadamente prestaciones accesorias | `acta-junta-sa-crea-extingue-anticipadamente-mer-0214` |
| MER-0215 | Escritura pública de creación o extinción anticipada de prestaciones accesorias en una SA | `escritura-publica-creacion-extincion-anticipada-mer-0215` |
| MER-0216 | Certificación de los acuerdos de la junta general extraordinaria de una sociedad anónima | `certificacion-acuerdos-junta-general-extraordinaria-mer-0216` |
| MER-0218 | Certificación del acuerdo de junta de nombrar auditor en una SL o SA | `certificacion-acuerdo-junta-nombrar-auditor-sl-sa-mer-0218` |
| MER-0219 | Anuncio de convocatoria de junta de una SA para cuentas anuales, cambio de objeto y de denominación | `anuncio-convocatoria-junta-sa-cuentas-anuales-cambio-mer-0219` |
| MER-0220 | Escritura pública de donación de acciones nominativas de una SA a un descendiente | `escritura-publica-donacion-acciones-nominativas-sa-mer-0220` |
| MER-0221 | Certificación del acta de junta universal de una SA que autoriza la venta de acciones | `certificacion-acta-junta-universal-sa-autoriza-venta-mer-0221` |
| MER-0223 | Escritura de constitución de una SA con aportaciones dinerarias y no dinerarias | `escritura-constitucion-sa-aportaciones-dinerarias-no-mer-0223` |
| MER-0224 | Estatutos sociales de una sociedad anónima | `estatutos-sociales-sociedad-anonima-mer-0224` |
| MER-0225 | Acta del consejo de una SA que delega facultades y nombra consejero delegado o comisión ejecutiva | `acta-consejo-sa-delega-facultades-nombra-consejero-mer-0225` |
| MER-0229 | Escritura pública de pérdida de la unipersonalidad de una SL o SA por transmisión de su capital | `escritura-publica-perdida-unipersonalidad-sl-sa-mer-0229` |
| MER-0230 | Escritura de constitución de una SL con aportaciones dinerarias, no dinerarias o mixtas | `escritura-constitucion-sl-aportaciones-dinerarias-no-mer-0230` |
| MER-0231 | Escritura de unipersonalidad sobrevenida de una SL por adquirir un socio todas las participaciones | `escritura-unipersonalidad-sobrevenida-sl-adquirir-mer-0231` |
| MER-0232 | Estatutos sociales de una sociedad limitada | `estatutos-sociales-sociedad-limitada-mer-0232` |
| MER-0233 | Acta de junta general de una SL, modelo general | `acta-junta-general-sl-modelo-general-mer-0233` |
| MER-0234 | Acta de junta general de una SL que acuerda la disolución | `acta-junta-general-sl-acuerda-disolucion-mer-0234` |
| MER-0235 | Escritura de requerimiento notarial de socios a los administradores de una SL para convocar junta | `escritura-requerimiento-notarial-socios-mer-0235` |
| MER-0236 | Escritura de apoderamiento mercantil otorgada por una sociedad anónima a favor de un tercero | `escritura-apoderamiento-mercantil-otorgada-sociedad-mer-0236` |
| MER-0237 | Escritura pública de donación de participaciones de una SL a un descendiente | `escritura-publica-donacion-participaciones-sl-mer-0237` |
| MER-0238 | Escritura pública de cese y nombramiento de administradores de una sociedad limitada | `escritura-publica-cese-nombramiento-administradores-mer-0238` |
| MER-0239 | Certificación del acuerdo de junta de cese y nombramiento de administradores de una SL | `certificacion-acuerdo-junta-cese-nombramiento-mer-0239` |
| MER-0240 | Escritura pública de reducción y ampliación simultánea de capital de una SL (operación acordeón) | `escritura-publica-reduccion-ampliacion-simultanea-mer-0240` |
| MER-0241 | Acta de junta de una SL que acuerda reducir y ampliar capital a la vez (operación acordeón) | `acta-junta-sl-acuerda-reducir-ampliar-capital-vez-mer-0241` |
| MER-0242 | Certificación del acuerdo de junta de una SL de reducir y ampliar capital a la vez (acordeón) | `certificacion-acuerdo-junta-sl-reducir-ampliar-capital-mer-0242` |
| MER-0243 | Acta de junta universal de una SL, modelo general | `acta-junta-universal-sl-modelo-general-mer-0243` |
| MER-0244 | Certificación del acuerdo de aprobación de las cuentas anuales de una SL | `certificacion-acuerdo-aprobacion-cuentas-anuales-sl-mer-0244` |
| MER-0245 | Certificación del acuerdo de junta de disolver una sociedad limitada | `certificacion-acuerdo-junta-disolver-sociedad-limitada-mer-0245` |
| MER-0246 | Certificación del acuerdo de junta de disolver y liquidar a la vez una sociedad limitada | `certificacion-acuerdo-junta-disolver-liquidar-vez-mer-0246` |
| MER-0247 | Escritura pública de liquidación de una sociedad limitada | `escritura-publica-liquidacion-sociedad-limitada-mer-0247` |
| MER-0248 | Acta de junta general de una SL que acuerda disolver y liquidar la sociedad a la vez | `acta-junta-general-sl-acuerda-disolver-liquidar-mer-0248` |
| MER-0249 | Certificación del acuerdo de junta que aprueba la liquidación de una sociedad limitada | `certificacion-acuerdo-junta-aprueba-liquidacion-mer-0249` |
| MER-0250 | Escritura pública del acuerdo de disolución de una sociedad limitada | `escritura-publica-acuerdo-disolucion-sociedad-limitada-mer-0250` |
| MER-0251 | Escritura pública de disolución y liquidación simultáneas de una sociedad limitada | `escritura-publica-disolucion-liquidacion-simultaneas-mer-0251` |
| MER-0252 | Acta de junta general de una SL que aprueba la liquidación de la sociedad | `acta-junta-general-sl-aprueba-liquidacion-sociedad-mer-0252` |
| MER-0253 | Certificación del acuerdo de junta de reactivar una sociedad disuelta | `certificacion-acuerdo-junta-reactivar-sociedad-disuelta-mer-0253` |
| MER-0254 | Certificación del acuerdo de aprobación de las cuentas anuales de una sociedad anónima | `certificacion-acuerdo-aprobacion-cuentas-anuales-mer-0254` |
| MER-0256 | Escritura pública de cambio de socio único en una sociedad limitada unipersonal | `escritura-publica-cambio-socio-unico-sociedad-limitada-mer-0256` |
| MER-0259 | Escritura de constitución de una sociedad unipersonal, limitada o anónima | `escritura-constitucion-sociedad-unipersonal-limitada-mer-0259` |
| MER-0260 | Escritura pública de cambio de socio único en una sociedad anónima unipersonal | `escritura-publica-cambio-socio-unico-sociedad-anonima-mer-0260` |
| MER-0262 | Escritura de unipersonalidad sobrevenida de una SA por pasar todas las acciones a un solo socio | `escritura-unipersonalidad-sobrevenida-sa-pasar-todas-mer-0262` |
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
| MER-0300 | Escritura pública de disolución y liquidación simultáneas de una sociedad anónima | `escritura-publica-disolucion-liquidacion-simultaneas-mer-0300` |
| MER-0301 | Certificación del acuerdo de junta de disolver y liquidar a la vez una sociedad anónima | `certificacion-acuerdo-junta-disolver-liquidar-vez-mer-0301` |
| MER-0302 | Acta de junta general extraordinaria de una SA que acuerda disolver y liquidar la sociedad a la vez | `acta-junta-general-extraordinaria-sa-acuerda-disolver-mer-0302` |
| MER-0304 | Escritura de constitución de sociedad con aportación de un bien ganancial | `escritura-constitucion-sociedad-aportacion-bien-mer-0304` |
| MER-0305 | Escritura de ampliación de capital con aportación de un bien ganancial | `escritura-ampliacion-capital-aportacion-bien-ganancial-mer-0305` |
| MER-0306 | Convocatoria de la junta general constitutiva de una sociedad | `convocatoria-junta-general-constitutiva-sociedad-mer-0306` |
| MER-0308 | Escritura de revocación de poder mercantil | `escritura-revocacion-poder-mercantil-mer-0308` |

### Comunicaciones, requerimientos y cartas (62)

| Código | Formulario | Skill |
|---|---|---|
| MER-0020 | Solicitud al Registro Mercantil de experto independiente para valorar aportaciones no dinerarias | `solicitud-registro-mercantil-experto-independiente-mer-0020` |
| MER-0049 | Solicitud de legalización telemática de libros contables de SL o SA | `solicitud-legalizacion-telematica-libros-contables-sl-mer-0049` |
| MER-0053 | Requerimiento de desembolso de aportaciones pendientes a un socio de una SA | `requerimiento-desembolso-aportaciones-pendientes-socio-mer-0053` |
| MER-0055 | Solicitud del socio de examinar la documentación de las cuentas anuales antes de la junta de SL | `solicitud-socio-examinar-documentacion-cuentas-anuales-mer-0055` |
| MER-0056 | Solicitud de certificación registral para el traslado de domicilio de una SL | `solicitud-certificacion-registral-traslado-domicilio-sl-mer-0056` |
| MER-0057 | Solicitud del socio de convocar junta de SL para acordar la disolución | `solicitud-socio-convocar-junta-sl-acordar-disolucion-mer-0057` |
| MER-0058 | Comunicación a los socios de la restitución de aportaciones por aumento de capital no suscrito | `comunicacion-socios-restitucion-aportaciones-aumento-mer-0058` |
| MER-0063 | Comunicación individual a los socios de la SL del acuerdo que genera derecho de separación | `comunicacion-individual-socios-sl-acuerdo-genera-mer-0063` |
| MER-0067 | Notificación al socio del acuerdo de su exclusión de una SL | `notificacion-socio-acuerdo-exclusion-sl-mer-0067` |
| MER-0082 | Notificación a la participada de haber superado el diez por ciento de su capital | `notificacion-participada-haber-superado-diez-ciento-mer-0082` |
| MER-0092 | Solicitud escrita de informes o aclaraciones sobre el orden del día antes de la junta | `solicitud-escrita-informes-aclaraciones-sobre-orden-mer-0092` |
| MER-0093 | Solicitud del accionista de examinar el libro registro de acciones nominativas | `solicitud-accionista-examinar-libro-registro-acciones-mer-0093` |
| MER-0094 | Solicitud de rectificación de error material en una inscripción del Registro Mercantil | `solicitud-rectificacion-error-material-inscripcion-mer-0094` |
| MER-0096 | Solicitud al registrador de experto que valore las participaciones del socio separado o excluido | `solicitud-registrador-experto-valore-participaciones-mer-0096` |
| MER-0097 | Notificación a la SL del representante común de los cotitulares de participaciones | `notificacion-sl-representante-comun-cotitulares-mer-0097` |
| MER-0098 | Notificación a la SL de la adquisición de participaciones sociales | `notificacion-sl-adquisicion-participaciones-sociales-mer-0098` |
| MER-0099 | Comunicación a la SL de la adquisición hereditaria de participaciones sociales | `comunicacion-sl-adquisicion-hereditaria-mer-0099` |
| MER-0100 | Solicitud de inscripción de una sucursal en el Registro Mercantil del domicilio social | `solicitud-inscripcion-sucursal-registro-mercantil-mer-0100` |
| MER-0101 | Solicitud de restitución de aportaciones por aumento de capital de SL no presentado a inscripción | `solicitud-restitucion-aportaciones-aumento-capital-sl-mer-0101` |
| MER-0102 | Solicitud de inscripción parcial en el Registro Mercantil | `solicitud-inscripcion-parcial-registro-mercantil-mer-0102` |
| MER-0103 | Solicitud de rectificación de errores en datos publicados en el BORME | `solicitud-rectificacion-errores-datos-publicados-borme-mer-0103` |
| MER-0105 | Notificación a interesados de la intención de rectificar el libro registro de acciones nominativas | `notificacion-interesados-intencion-rectificar-libro-mer-0105` |
| MER-0106 | Notificación notarial a la participada de haber superado el diez por ciento de su capital | `notificacion-notarial-participada-haber-superado-diez-mer-0106` |
| MER-0112 | Solicitud de duplicado o renovación de la certificación de denominación social | `solicitud-duplicado-renovacion-certificacion-mer-0112` |
| MER-0113 | Solicitud de certificación negativa de denominación social al Registro Mercantil Central | `solicitud-certificacion-negativa-denominacion-social-mer-0113` |
| MER-0114 | Solicitud de certificación registral del nombramiento de administradores | `solicitud-certificacion-registral-nombramiento-mer-0114` |
| MER-0115 | Solicitud del accionista de certificación del libro registro de acciones nominativas | `solicitud-accionista-certificacion-libro-registro-mer-0115` |
| MER-0126 | Notificación al Registro del cambio de titular de la facultad certificante | `notificacion-registro-cambio-titular-facultad-mer-0126` |
| MER-0132 | Carta de encargo de auditoría de cuentas para ejercicios sucesivos | `carta-encargo-auditoria-cuentas-ejercicios-sucesivos-mer-0132` |
| MER-0133 | Solicitud al letrado de la Administración de Justicia de convocatoria de junta extraordinaria de SA | `solicitud-letrado-administracion-justicia-convocatoria-mer-0133` |
| MER-0140 | Comunicación a los socios de la modificación del régimen de transmisión de participaciones | `comunicacion-socios-modificacion-regimen-transmision-mer-0140` |
| MER-0141 | Carta circular para votación escrita y sin sesión del consejo de administración de una SA | `carta-circular-votacion-escrita-sin-sesion-consejo-mer-0141` |
| MER-0143 | Comunicación escrita a los socios de una SL para ejercer el derecho de preferencia | `comunicacion-escrita-socios-sl-ejercer-derecho-mer-0143` |
| MER-0144 | Notificación a los acreedores del acuerdo de reducción de capital de una SL para su oposición | `notificacion-acreedores-acuerdo-reduccion-capital-sl-mer-0144` |
| MER-0147 | Solicitud de experto independiente para informar sobre adquisiciones onerosas de una SA | `solicitud-experto-independiente-informar-sobre-mer-0147` |
| MER-0148 | Solicitud de experto independiente sobre aportaciones no dinerarias en aumentos de capital de SA | `solicitud-experto-independiente-sobre-aportaciones-no-mer-0148` |
| MER-0150 | Solicitud de consentimiento a los accionistas para aumentar capital elevando el valor nominal | `solicitud-consentimiento-accionistas-aumentar-capital-mer-0150` |
| MER-0152 | Solicitud de auditor al Registro Mercantil que certifique los créditos a compensar en una SA | `solicitud-auditor-registro-mercantil-certifique-mer-0152` |
| MER-0153 | Solicitud de auditor al Registro Mercantil sobre las reservas con cargo a las que se aumenta capital | `solicitud-auditor-registro-mercantil-sobre-reservas-mer-0153` |
| MER-0159 | Comunicación de que el aumento de capital de SA queda sin efecto por suscripción incompleta | `comunicacion-aumento-capital-sa-queda-sin-efecto-mer-0159` |
| MER-0164 | Solicitud pública de representación para la junta general de una SA | `solicitud-publica-representacion-junta-general-sa-mer-0164` |
| MER-0165 | Solicitud de complemento de la convocatoria de la junta de una SA | `solicitud-complemento-convocatoria-junta-sa-mer-0165` |
| MER-0169 | Carta de separación del socio por cambio de objeto, duración, régimen de transmisión o domicilio | `carta-separacion-socio-cambio-objeto-duracion-regimen-mer-0169` |
| MER-0170 | Solicitud al Registro Mercantil de auditor que determine el valor de acciones o participaciones | `solicitud-registro-mercantil-auditor-determine-valor-mer-0170` |
| MER-0173 | Carta de comunicación de actividades con conflicto de intereses por un administrador | `carta-comunicacion-actividades-conflicto-intereses-mer-0173` |
| MER-0175 | Carta de manifestaciones de la administración al auditor | `carta-manifestaciones-administracion-auditor-mer-0175` |
| MER-0176 | Carta de convocatoria de junta de SA para reducir el capital social | `carta-convocatoria-junta-sa-reducir-capital-social-mer-0176` |
| MER-0191 | Carta de representación de un socio de SL para asistir a la junta general | `carta-representacion-socio-sl-asistir-junta-general-mer-0191` |
| MER-0200 | Solicitud del accionista al consejo de la documentación de las cuentas anuales antes de la junta | `solicitud-accionista-consejo-documentacion-cuentas-mer-0200` |
| MER-0205 | Requerimiento para elevar a escritura pública la venta privada de participaciones de una SL | `requerimiento-elevar-escritura-publica-venta-privada-mer-0205` |
| MER-0257 | Comunicación del administrador de una SL a un socio de su propósito de rectificar el libro de socios | `comunicacion-administrador-sl-socio-proposito-mer-0257` |
| MER-0258 | Requerimiento notarial a los administradores de una SA para que convoquen junta extraordinaria | `requerimiento-notarial-administradores-sa-convoquen-mer-0258` |
| MER-0261 | Requerimiento a los administradores de una SA para que un notario levante acta de la junta general | `requerimiento-administradores-sa-notario-levante-acta-mer-0261` |
| MER-0264 | Solicitud del accionista de autorización del órgano de administración para vender acciones | `solicitud-accionista-autorizacion-organo-mer-0264` |
| MER-0267 | Solicitud de socios minoritarios de una SA para convocar junta general ordinaria o extraordinaria | `solicitud-socios-minoritarios-sa-convocar-junta-mer-0267` |
| MER-0268 | Comunicación del administrador de una SL a los socios del embargo de participaciones sociales | `comunicacion-administrador-sl-socios-embargo-mer-0268` |
| MER-0270 | Solicitud de un socio de SL de certificación del libro registro de socios | `solicitud-socio-sl-certificacion-libro-registro-socios-mer-0270` |
| MER-0271 | Solicitud de socios de una SL para convocar junta que apruebe las cuentas anuales | `solicitud-socios-sl-convocar-junta-apruebe-cuentas-mer-0271` |
| MER-0272 | Solicitud de un socio de SL de consentimiento para transmitir sus participaciones sociales | `solicitud-socio-sl-consentimiento-transmitir-mer-0272` |
| MER-0274 | Requerimiento a los administradores de una SL para que un notario levante acta de la junta general | `requerimiento-administradores-sl-notario-levante-acta-mer-0274` |
| MER-0303 | Carta de socios a los administradores solicitando convocar la junta general de una SL o SA | `carta-socios-administradores-solicitando-convocar-mer-0303` |
| MER-0309 | Solicitud de convocatoria de junta extraordinaria de SL por socios con el 5 por ciento del capital | `solicitud-convocatoria-junta-extraordinaria-sl-socios-mer-0309` |

### Escritos de trámite y otros (36)

| Código | Formulario | Skill |
|---|---|---|
| MER-0001 | Depósito de cuentas anuales 2025 en modelo oficial abreviado | `deposito-cuentas-anuales-2025-modelo-oficial-abreviado-mer-0001` |
| MER-0002 | Depósito de cuentas anuales 2025 en modelo oficial para PYMES | `deposito-cuentas-anuales-2025-modelo-oficial-pymes-mer-0002` |
| MER-0006 | Depósito de cuentas anuales 2025 en modelo oficial normal | `deposito-cuentas-anuales-2025-modelo-oficial-normal-mer-0006` |
| MER-0007 | Depósito de cuentas anuales consolidadas 2025 en modelo oficial | `deposito-cuentas-anuales-consolidadas-2025-modelo-mer-0007` |
| MER-0022 | Escrito de aceptación del cargo de administrador de una SL o SA | `escrito-aceptacion-cargo-administrador-sl-sa-mer-0022` |
| MER-0047 | Instancia de solicitud de legalización de libros en el Registro Mercantil | `instancia-solicitud-legalizacion-libros-registro-mer-0047` |
| MER-0048 | Relación de libros con su firma digital para legalizar en el Registro Mercantil | `relacion-libros-firma-digital-legalizar-registro-mer-0048` |
| MER-0052 | Anexo al acta de junta de SA sobre quórum y suspensión del voto de las acciones propias | `anexo-acta-junta-sa-sobre-quorum-suspension-voto-mer-0052` |
| MER-0060 | Separación del socio por desacuerdo con un acuerdo social o falta de reparto de dividendos | `separacion-socio-desacuerdo-acuerdo-social-falta-mer-0060` |
| MER-0061 | Documento de acuerdo sobre el valor de las participaciones del socio que se separa de una SL | `documento-acuerdo-sobre-valor-participaciones-socio-mer-0061` |
| MER-0066 | Lista de asistentes a la junta general de una SL | `lista-asistentes-junta-general-sl-mer-0066` |
| MER-0087 | Delegación de voto de un consejero en otro para asistir al consejo de administración | `delegacion-voto-consejero-otro-asistir-consejo-mer-0087` |
| MER-0089 | Título de acción de una sociedad anónima | `titulo-accion-sociedad-anonima-mer-0089` |
| MER-0104 | Respuesta de los administradores que envía o deniega información sobre el orden del día de la junta | `respuesta-administradores-envia-deniega-informacion-mer-0104` |
| MER-0110 | Escrito de renuncia al cargo de administrador de una SL o SA | `escrito-renuncia-cargo-administrador-sl-sa-mer-0110` |
| MER-0111 | Diligencia de aprobación diferida del acta de la junta general | `diligencia-aprobacion-diferida-acta-junta-general-mer-0111` |
| MER-0116 | Escrito del socio que reclama el pago de dividendos no prescritos | `escrito-socio-reclama-pago-dividendos-no-prescritos-mer-0116` |
| MER-0118 | Hoja del libro registro de acciones nominativas | `hoja-libro-registro-acciones-nominativas-mer-0118` |
| MER-0131 | Sociedad mercantil irregular (contrato) | `sociedad-mercantil-irregular-contrato-mer-0131` |
| MER-0135 | Votación escrita y sin sesión del consejo de SA sobre aceptación, nombramientos y reparto de cargos | `votacion-escrita-sin-sesion-consejo-sa-sobre-mer-0135` |
| MER-0137 | Publicación de la propuesta de compra de acciones propias para reducir capital de una SA | `publicacion-propuesta-compra-acciones-propias-reducir-mer-0137` |
| MER-0156 | Escrito del secretario cesado que se da por enterado del nombramiento de su sucesor en el consejo | `escrito-secretario-cesado-da-enterado-nombramiento-mer-0156` |
| MER-0157 | Propuesta de acuerdo de reducción y aumento simultáneo de capital de una SA | `propuesta-acuerdo-reduccion-aumento-simultaneo-capital-mer-0157` |
| MER-0163 | Oferta de suscripción preferente de nuevas acciones en el aumento de capital de una SA | `oferta-suscripcion-preferente-nuevas-acciones-aumento-mer-0163` |
| MER-0202 | Artículo estatutario de sometimiento a arbitraje ante una cámara de comercio | `articulo-estatutario-sometimiento-arbitraje-ante-mer-0202` |
| MER-0217 | Escrito de autorización para que otra persona represente al socio en la junta general de una SL o SA | `escrito-autorizacion-otra-persona-represente-socio-mer-0217` |
| MER-0222 | Resguardo provisional de acciones de una sociedad anónima | `resguardo-provisional-acciones-sociedad-anonima-mer-0222` |
| MER-0226 | Título al portador representativo de una o varias acciones de una SA | `titulo-portador-representativo-varias-acciones-sa-mer-0226` |
| MER-0227 | Programa de fundación de una SA por suscripción pública de acciones (fundación sucesiva) | `programa-fundacion-sa-suscripcion-publica-acciones-mer-0227` |
| MER-0228 | Escrito de aceptación del cargo de administrador de una SA con firma legitimada ante notario | `escrito-aceptacion-cargo-administrador-sa-firma-mer-0228` |
| MER-0255 | Escrito de un socio de SL oponiéndose a la rectificación del libro registro de socios | `escrito-socio-sl-oponiendose-rectificacion-libro-mer-0255` |
| MER-0265 | Endoso de una acción nominativa de una sociedad anónima | `endoso-accion-nominativa-sociedad-anonima-mer-0265` |
| MER-0282 | Boletín de suscripción de acciones en la fundación sucesiva de una sociedad anónima | `boletin-suscripcion-acciones-fundacion-sucesiva-mer-0282` |
| MER-0283 | Título nominativo representativo de una o varias acciones de una sociedad anónima | `titulo-nominativo-representativo-varias-acciones-mer-0283` |
| MER-0286 | Lista de asistentes a la junta general de accionistas de una sociedad anónima | `lista-asistentes-junta-general-accionistas-sociedad-mer-0286` |
| MER-0307 | Instancia al Registro Mercantil para legalizar los libros del empresario | `instancia-registro-mercantil-legalizar-libros-mer-0307` |
