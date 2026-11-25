# Formularios jurídicos de España para Claude · Mercantil

12 plugins de formularios de Mercantil, uno por materia. Cada formulario es una skill que Claude rellena paso a paso con los datos del caso y entrega en Word tal cual es el formulario (Times New Roman 11, interlineado 1,15 y texto justificado): 844 skills en total, contando la skill `indice` de cada plugin, que sirve para encontrar el formulario adecuado.

Todas las skills trabajan con **Jurisprudenciator** (https://jurisprudenciator.lexiaipro.org): antes de redactar comprueban que el conector responde y verifican en fuentes oficiales las normas que cita el formulario. Sin Jurisprudenciator conectado, las skills no redactan. Normativa revisada el 25-11-2026.

Las demás jurisdicciones están en repositorios propios: [Civil](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana), [Seguridad Social](https://github.com/DerechoVirtual/formularios-juridicos-seguridad-social-espana), [Administrativo y Tributario](https://github.com/DerechoVirtual/formularios-juridicos-administrativo-tributario-espana), [Laboral](https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana), [Penal](https://github.com/DerechoVirtual/formularios-juridicos-penal-espana).

## Instalación

En Claude Code:

```
/plugin marketplace add DerechoVirtual/formularios-juridicos-mercantil-espana
/plugin install formularios-juntas-y-actas-de-sociedades@formularios-juridicos-mercantil-espana
```

Cada plugin ocupa contexto en la conversación, así que conviene instalar solo los de las materias con las que se trabaja.

En Claude (web, escritorio y Cowork) se puede añadir este repositorio desde **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-juridicos-mercantil-espana`, o subir cada plugin como ZIP. Los ZIP están en la página de [versiones](https://github.com/DerechoVirtual/formularios-juridicos-mercantil-espana/releases/latest).

## Plugins

| Plugin | Contenido | Skills | ZIP |
|---|---|---:|---|
| `formularios-juntas-y-actas-de-sociedades` | Juntas, consejos y actas de sociedades de capital | 172 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-mercantil-espana/releases/latest/download/formularios-juntas-y-actas-de-sociedades.zip) |
| `formularios-sociedades-de-capital` | Sociedades de capital: constitución, capital, administradores y cuentas | 140 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-mercantil-espana/releases/latest/download/formularios-sociedades-de-capital.zip) |
| `formularios-fusiones-y-escisiones` | Fusiones, escisiones y transformaciones de sociedades | 56 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-mercantil-espana/releases/latest/download/formularios-fusiones-y-escisiones.zip) |
| `formularios-cooperativas-y-otras-sociedades` | Cooperativas, sociedades laborales y otras formas de empresa | 113 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-mercantil-espana/releases/latest/download/formularios-cooperativas-y-otras-sociedades.zip) |
| `formularios-agencia-distribucion-y-franquicia` | Agencia, distribución, franquicia y colaboración entre empresas | 35 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-mercantil-espana/releases/latest/download/formularios-agencia-distribucion-y-franquicia.zip) |
| `formularios-contratos-mercantiles` | Contratos mercantiles: compraventa, suministro, transporte y servicios | 105 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-mercantil-espana/releases/latest/download/formularios-contratos-mercantiles.zip) |
| `formularios-banca-financiacion-y-garantias` | Banca, financiación, valores y garantías | 69 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-mercantil-espana/releases/latest/download/formularios-banca-financiacion-y-garantias.zip) |
| `formularios-seguros` | Seguros: pólizas, coberturas y reclamaciones | 12 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-mercantil-espana/releases/latest/download/formularios-seguros.zip) |
| `formularios-marcas-patentes-y-propiedad-intelectual` | Marcas, patentes y propiedad intelectual | 54 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-mercantil-espana/releases/latest/download/formularios-marcas-patentes-y-propiedad-intelectual.zip) |
| `formularios-tecnologia-y-proteccion-de-datos` | Contratos tecnológicos, comercio electrónico y protección de datos | 33 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-mercantil-espana/releases/latest/download/formularios-tecnologia-y-proteccion-de-datos.zip) |
| `formularios-pleitos-mercantiles-y-concurso` | Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso | 34 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-mercantil-espana/releases/latest/download/formularios-pleitos-mercantiles-y-concurso.zip) |
| `formularios-traspasos-y-acuerdos-de-empresa` | Traspasos de negocio, confidencialidad y acuerdos de empresa | 21 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-mercantil-espana/releases/latest/download/formularios-traspasos-y-acuerdos-de-empresa.zip) |

## Estructura

```
.claude-plugin/marketplace.json  catálogo del marketplace
plugins/<plugin>/                .claude-plugin/plugin.json, .mcp.json, skills/<skill>/SKILL.md y assets/formulario.md, README.md, PRIVACY.md, LICENSE
```

## Aviso

Los documentos que se generan son borradores que debe revisar un abogado; no constituyen asesoramiento jurídico. Las skills no guardan datos del cliente y las consultas a Jurisprudenciator describen el problema jurídico, no los datos personales.

Soporte: https://jurisprudenciator.lexiaipro.org/incidencias · Licencia: ver [LICENSE](LICENSE).
