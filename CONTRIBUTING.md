# Guía de contribución

Para mantener el proyecto ordenado y con un historial limpio, seguimos este flujo de trabajo obligatorio:

## 1. Ramas de vida corta

⚠️ **IMPORTANTE:** La rama `main` de este repositorio está protegida. No es posible hacer `git push` directamente a `main`. Todo cambio entra por Pull Request.

Antes de escribir una sola línea de código, debes crear una rama local para tu tarea. Tu rama siempre debe nacer desde `main` completamente actualizada.

1. Regresa a la rama principal y asegúrate de traer los últimos cambios del servidor con `git pull origin main`.

2. Crea y muévete a tu nueva rama utilizando un nombre descriptivo y en inglés:

```bash
git checkout -b prefix/task-description
```
Los siguientes son los prefijos permitidos:

* `feat/` para nuevas características.
* `fix/` para corrección de errores.
* `docs/` para cambios en la documentación.
* `chore/` para tareas de mantenimiento o dependencias.

## 2. Mensajes de commit

Utilizamos **Conventional Commits** en idioma **Inglés**. El formato del mensaje debe ser: `tipo: descripción corta en minúsculas`

### Ejemplos

* `feat: add login with google`
* `fix: resolve timeout error on checkout`
* `docs: update installation steps in README.md`
* `chore: upgrade dependency lodash to version 4.17.21`

## 3. Pull Requests (PR) y Revisión

Una vez que hayas terminado de programar y tus commits locales estén listos, es hora de enviarlos a GitHub para su revisión.

1. Envía tu rama local al servidor remoto con el comando:

```bash
git push -u origin prefix/task-description
```

2. Entra a la página del repositorio en GitHub, y abre una nueva PR con tus cambios.

3. **El título del PR:** Como el repositorio realiza un _Squash merge_ al final, **el título de tu PR se convertirá en el mensaje final en** `main`. Por lo tanto, el título del PR debe seguir obligatoriamente el formato de Conventional Commits y estar escrito en inglés.

4. **La plantilla:** Notarás que el cuerpo del PR se rellena **automáticamente** con una plantilla de texto. No la borres; completa todos los campos solicitados, ya que sirve para los revisores.

## 4. Autorrevisión

Antes de avisar al equipo para que revise tu código, haz una inspección tú mismo:

1. Ve a la pestaña "**Files changed**" dentro de tu PR en GitHub
2. Revisa línea por línea tu código en busca de logs de prueba olvidados, código muerto o problemas visuales de formateo.
3. Haz merge con squash y verifica que la rama se elimina automáticamente.
