# Convenciones de BroLos

## Repos
- Nombres en kebab-case (`mi-herramienta`). Los repos antiguos conservan su nombre.
- Rama principal: `main`.

## Flujo de trabajo
- Nada de push directo a `main`: todo entra por Pull Request (convención; el plan Free no lo fuerza en repos privados).
- Cada cambio nace de un ticket de Linear (equipo BroLos, prefijo `BRO`).
- Nombre de rama: usa "Copy git branch name" en Linear (contiene `bro-<n>`), así la rama y la PR se vinculan solas al ticket.
- Título de la PR con el ID: `BRO-<n>: descripción`. Pon `Fixes BRO-<n>` en el cuerpo para cerrar el ticket al hacer merge.

## Secretos
- Nunca en el código ni en el historial de git.
- Cada repo incluye un `.env.example` con los nombres de las variables (sin valores); los `.env` reales van en `.gitignore`.
- CI/despliegue: GitHub Secrets a nivel de repo (`gh secret set NOMBRE -R brolos-dev/<repo>`).
- Los `.env` locales se comparten entre owners fuera de banda, nunca por commits, issues ni PRs.

