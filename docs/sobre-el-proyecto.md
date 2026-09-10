# Sobre el dataset

Este dataset proviene de un pipeline personal de automatización de threat
intelligence: los boletines de seguridad se analizan con un modelo de lenguaje
y, cuando corresponde, el resultado se agrega como una entrada nueva a un
listado de indicadores de compromiso.

## Por qué se comparte solo el dataset aquí

El código fuente y la infraestructura como código del pipeline están
publicados en un repositorio distinto (`github.com/mallendec/soc-threat-intel-pipeline`),
asociado a otra cuenta. Este repositorio (`matias00allende`) es una cuenta
independiente y contiene únicamente el dataset de salida - el resultado del
pipeline, no su implementación.

## Cómo verificar que el dataset es real

El archivo se sirve en producción desde dos dominios públicos distintos sobre
un mismo objeto de almacenamiento. Una petición `curl -I` contra ambos
devuelve cabeceras HTTP idénticas (mismo `Content-Length` y mismo `ETag`), lo
que confirma que se trata del mismo objeto. Ese archivo es el que se copia en
`data/hash_sha256.txt` de este repositorio.

## Referencias

- Repositorio del pipeline completo: `github.com/mallendec/soc-threat-intel-pipeline`
