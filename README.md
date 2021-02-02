# Commits Convencionales
## Introduccion
La especificación de [Commit Convencionales](https://www.conventionalcommits.org/es/v1.0.0-beta.3/) es una convención liviana que se aplica a los mensajes de los commits. Esta especificación proporciona un conjunto fácil de reglas para crear un historial de commits explícito; Esta convención se ajusta a SemVer, al describir las características, correcciones y cambios que rompen la compatibilidad en los mensajes de los commits.

El mensaje del commit debe estar estructurado de la siguiente forma:
```
<type>(<scope>): <subject>
<Línea en blanco>
<body>
<Línea en blanco>
<footer>
```

## Type
- **BREAKING CHANGE**: introduce un cambio que rompe la compatibilidad en el uso de la API (se correlaciona con MAJOR en el [Versionado Semantico](https://semver.org/)).

- **feat**: Añade una nueva funcionalidad (equivalente a un `MINOR` en [Versionado Semantico](https://semver.org/)).

- **fix**: Correcion de un bug (equivalente a un `PATCH` en [Versionado Semantico](https://semver.org/)).

- **docs**: Cambios en la documentacion.

- **style**: Cambio de estilo en el código (punto y coma, sangría...).

- **refactor**: Refactorización de codigo que ni añade una funcionalidad ni arregla un error.

- **perf**: Cambio en el código que mejora el rendimiento del código.

- **test**: Añadir nuevos tests o arreglar los ya existentes.

- **chore**: Cambios en el proceso de compilado o en el uso de herramientas externas (ej.: bump una dependencia en package.json).

## Scope
El scope se refiere a la parte del código en el que se está realizando un cambio, es decir, a qué clase o archivo afecta, si es para algún navegador específico, si es sobre una herramienta que se ha añadido, etc.

## Subject
Esta es la parte que realmente describe lo que hemos cambiado dentro del scope. Debemos aplicar las siguientes reglas:
- Utilizar el imperativo
- No poner mayúscula en la primera letra
- No añadir un punto (.) al final de la frase
- Evitar escribir más de 50 caracteres

## Body

El body sirve para explicar qué cambios hemos hecho y por qué los hemos hecho. No todos los commits son lo suficientemente complejos como para tener que escribir un body y a veces basta con escribir un buen header.

## Footer
El footer también es opcional y suele utilizarse para añadir enlaces a algún issue tracker que estés utilizando como Jira, Redmine o Clubhouse.

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
- [Angular.js](https://github.com/angular/angular.js/blob/master/DEVELOPERS.md#-git-commit-guidelines)
