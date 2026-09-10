# Dataset de hashes IOC (SHA-256)

Snapshot público de indicadores de compromiso (hashes SHA-256), generado por un
pipeline personal de automatización de threat intelligence.

## Qué es esto

Copia estática de un feed de indicadores de compromiso, tomada en una fecha
determinada. Cada línea del archivo `data/hash_sha256.txt` tiene el formato:

```
<hash_sha256> SHA256_<FAMILIA_O_CAMPAÑA>
```

Un hash por línea, separado por un espacio, con la familia o campaña asociada
en mayúsculas como segunda columna. El archivo se generó automáticamente; no
fue curado ni filtrado a mano línea por línea.

## Qué NO es esto

- **No es el repositorio del pipeline.** El código fuente y la
  infraestructura que generan este archivo están en un repositorio distinto:
  `github.com/mallendec/soc-threat-intel-pipeline`. Esta cuenta
  (`matias00allende`) es independiente y contiene **únicamente el dataset**,
  no el pipeline.
- **No es un feed en vivo.** Es una fotografía tomada en una fecha
  determinada (ver `CHANGELOG.md`). El sistema real actualiza el feed de
  forma continua; este snapshot no se sincroniza automáticamente.
- **No es una fuente de verdad para bloqueo automatizado.** Es material de
  referencia y estudio. Para uso operacional real, cruzar siempre contra
  fuentes de threat intelligence propias y vigentes.

## Aviso de falsos positivos

Este listado proviene de un proceso de clasificación asistido por un modelo
de lenguaje sobre boletines públicos de seguridad. Como todo sistema de
clasificación automatizada, **puede contener falsos positivos** (hashes
marcados como asociados a una familia o campaña sin confirmación humana
individual de cada caso) y, en menor medida, podría no capturar todas las
variantes de una amenaza (falsos negativos). No usar este archivo como única
fuente de bloqueo en un entorno productivo sin validación adicional.

## Contenido del snapshot

- 20.080 indicadores (hashes SHA-256), uno por línea.
- Cientos de familias o campañas distintas identificadas como segunda columna.
- Ver `CHANGELOG.md` para la fecha exacta de captura.

## Licencia

Este dataset se publica bajo **CC0 1.0 Universal** (dominio público). Puede
usarse, copiarse, modificarse y redistribuirse libremente, sin atribución
obligatoria. Ver `LICENSE`.

## Contacto

Matías Allende - matias.allende.contreras@gmail.com
