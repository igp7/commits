# Commits Convencionales
## Introduccion
La especificación de [Commit Convencionales](https://www.conventionalcommits.org/es/v1.0.0-beta.3/) es una convención liviana que se aplica a los mensajes de los commits. Esta especificación proporciona un conjunto fácil de reglas para crear un historial de commits explícito; Esta convención se ajusta a SemVer, al describir las características, correcciones y cambios que rompen la compatibilidad en los mensajes de los commits.

El mensaje del commit debe estar estructurado de la siguiente forma:
```
/^(revert: )?(feat|fix|docs|style|refactor|perf|test|chore)(\(.+\))?: .{1,50}/
```

## Tipos de commit
- **BREAKING CHANGE**: introduce un cambio que rompe la compatibilidad en el uso de la API (se correlaciona con MAJOR en el [Versionado Semantico](https://semver.org/)).

- **feat**: Añade una nueva funcionalidad (equivalente a un `MINOR` en [Versionado Semantico](https://semver.org/)).

- **fix**: Correcion de un bug (equivalente a un `PATCH` en [Versionado Semantico](https://semver.org/)).

- **docs**: Cambios en la documentacion.

- **style**: Cambio de estilo en el código (punto y coma, sangría...).

- **refactor**: Refactorización de codigo sin cambiar la API pública.

- **perf**: Actualización del funcionamiento del código.

- **test**: Añadir un test de una funcionalidad existente.

- **chore**: Actualizar algo sin impacto en el usuario (ej.: bump una dependencia en package.json).

## Ejemplos de Commits Convencionales
Hay varias formas de crear un Commits Convencionale:

- Uno de las formas es agregar un ámbito(documento, fichero, ...) al tipo de commit para proveer información contextual adicional y se escribe entre paréntesis, e.g., `feat(parser): add ability to parse arrays`:
```sh
# Añadir una nueva funcionalidad o característica
git commit -m "feat(lang): added polish language"
```

- Otra forma es no agregar un ámbito(documento, fichero, ...):
```sh
# Corregir la documentación
git commit -m "docs: correct spelling of CHANGELOG"
```

## Documentación de referencia

- [Commits Convencionales](https://www.conventionalcommits.org/es/v1.0.0-beta.3/)

- [Post - Enhance your git log with conventional commits](https://dev.to/maxpou/enhance-your-git-log-with-conventional-commits-3ea4)

- Generacion de changelog: [conventional-changelog](https://github.com/conventional-changelog/conventional-changelog/tree/master/packages/conventional-changelog-cli)
