---
name: indice
description: "Índice de los 11 formularios de Seguros: pólizas, coberturas y reclamaciones. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Seguros: pólizas, coberturas y reclamaciones: índice de formularios

> Plugin `formularios-seguros` · 11 formularios · normativa revisada el 24-11-2026.

## Qué es

Para el contrato de seguro: pólizas (vida, responsabilidad civil, defensa jurídica…), declaraciones del asegurado, comunicación del siniestro y reclamaciones a la aseguradora conforme a la Ley de Contrato de Seguro.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Póliza de seguro de responsabilidad civil profesional»
- «Comunicación del siniestro a la aseguradora»
- «Reclamación a la aseguradora por rechazo del siniestro»

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

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-seguros:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado: el formulario está al final de ese fichero y la guía del tema es el `marco.md` de esta carpeta.

### Contratos, pactos y cláusulas (9)

| Código | Formulario | Skill |
|---|---|---|
| MER-0686 | Póliza de seguro de transporte marítimo de mercancías | `poliza-seguro-transporte-maritimo-mercancias-mer-0686` |
| MER-0687 | Póliza de seguro de vida con condiciones particulares | `poliza-seguro-vida-condiciones-particulares-mer-0687` |
| MER-0688 | Póliza de seguro de responsabilidad civil con condiciones particulares | `poliza-seguro-responsabilidad-civil-condiciones-mer-0688` |
| MER-0689 | Contrato de apoderamiento a una agencia de suscripción de seguros | `contrato-apoderamiento-agencia-suscripcion-seguros-mer-0689` |
| MER-0690 | Póliza de seguro de responsabilidad civil de corredores de seguros | `poliza-seguro-responsabilidad-civil-corredores-seguros-mer-0690` |
| MER-0691 | Póliza de seguro de transporte terrestre de mercancías (modelo) | `poliza-seguro-transporte-terrestre-mercancias-modelo-mer-0691` |
| MER-0692 | Póliza de seguro de responsabilidad civil de procuradores | `poliza-seguro-responsabilidad-civil-procuradores-mer-0692` |
| MER-0694 | Condiciones generales del seguro de accidentes | `condiciones-generales-seguro-accidentes-mer-0694` |
| MER-0696 | Póliza tipo de seguro multirriesgo del hogar | `poliza-tipo-seguro-multirriesgo-hogar-mer-0696` |

### Escritos de trámite y otros (2)

| Código | Formulario | Skill |
|---|---|---|
| MER-0693 | Seguro de vida entera mixto de fallecimiento y supervivencia con garantías complementarias | `seguro-vida-entera-mixto-fallecimiento-supervivencia-mer-0693` |
| MER-0695 | Seguro de vida temporal de fallecimiento con garantías complementarias | `seguro-vida-temporal-fallecimiento-garantias-mer-0695` |
