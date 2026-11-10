# ProyBC-Devlights

Repositorio compartido del equipo.

## Flujo de trabajo

La rama `main` contiene los cambios integrados. Cada tarea se desarrolla en una rama propia y se integra mediante un pull request revisado por otro integrante.

### Empezar una tarea

```bash
git switch main
git pull --ff-only origin main
git switch -c feat/nombre-de-la-tarea
```

Usar `feat/` para funcionalidades, `fix/` para correcciones y `docs/` para documentación.

### Compartir los cambios

```bash
git status
git add ruta/del/archivo
git commit -m "Describe el cambio realizado"
git push -u origin HEAD
```

Después, abrir un pull request en GitHub hacia `main` y solicitar la revisión de un compañero. Evitar subir cambios directamente a `main`.

## Incorporarse al equipo

Aceptar la invitación al repositorio y ejecutar:

```bash
git clone https://github.com/NazarenoAc/ProyBC-Devlights.git
cd ProyBC-Devlights
```

Luego crear una rama siguiendo los pasos anteriores. No subir contraseñas, tokens ni archivos con credenciales.
