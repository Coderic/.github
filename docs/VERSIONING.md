# Versionado semántico en Coderic

## Política

Las librerías publicadas (`@coderic/*`) y los servicios con release siguen [SemVer 2.0.0](https://semver.org/lang/es/):

- **MAJOR**: cambio incompatible en la API o en el contrato HTTP documentado.
- **MINOR**: funcionalidad compatible hacia atrás.
- **PATCH**: corrección compatible hacia atrás.

## Changelog

Cada paquete publicado mantiene un `CHANGELOG.md` en formato [Keep a Changelog](https://keepachangelog.com/es-ES/1.1.0/). Partir de `CHANGELOG.template.md` en este repositorio.

## Releases

1. Mover entradas de `[Unreleased]` a la versión nueva.
2. Actualizar `version` en `package.json` (o el descriptor del servicio).
3. Etiquetar `vMAJOR.MINOR.PATCH` y publicar el release en GitHub.
4. Anunciar deprecaciones al menos una MINOR antes de un MAJOR que las retire.

## Script de apoyo

En el meta-repositorio: `node scripts/changelog-entry.mjs --version X.Y.Z --type added|changed|fixed|… --text "…"`.
