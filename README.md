# ProyBC-Devlights

Repositorio compartido del equipo.

## Flujo de trabajo

Flujo del equipo: rama personal → `DEV` → `main`.

- `main`: versión estable, con cambios ya probados y aprobados.
- `DEV`: integración de los cambios del equipo y pruebas conjuntas.
- `branch-naza`, `branch-fabri`, `branch-nico` y `branch-valen`: ramas personales, creadas desde `DEV`.

Los pull requests de las ramas personales se dirigen a `DEV`. Después de integrar y probar los cambios en `DEV`, abrir un pull request de `DEV` hacia `main`. Evitar subir cambios directamente a `DEV` o `main`.

### Empezar a trabajar en la rama personal

```bash
git fetch origin
git switch branch-naza
git pull --ff-only origin branch-naza
```

Las cuatro ramas ya están creadas. Reemplazar `branch-naza` por la rama correspondiente: `branch-fabri`, `branch-nico` o `branch-valen`.

### Actualizar la rama personal antes de trabajar

Con los cambios anteriores guardados en un commit:

```bash
git switch branch-naza
git fetch origin
git merge origin/DEV
```

Si aparecen conflictos, resolverlos y completar el commit antes de continuar.

### Compartir los cambios

```bash
git status
git add ruta/del/archivo
git commit -m "Describe el cambio realizado"
git push -u origin HEAD
```

Después, abrir un pull request en GitHub con base `DEV` y solicitar la revisión de un compañero. Conservar las ramas personales después de integrarlas para seguir trabajando en ellas.

### Publicar una versión estable

1. Integrar los pull requests aprobados en `DEV`.
2. Probar en `DEV` los cambios combinados del equipo.
3. Corregir los problemas mediante ramas personales y nuevos pull requests hacia `DEV`.
4. Cuando todo esté correcto, abrir y revisar un pull request con base `main` y origen `DEV`.
5. Integrarlo y conservar la rama `DEV` para el siguiente ciclo.

Para conservar un historial compartido entre estas ramas persistentes, usar merge commits al integrar los pull requests.

## Incorporarse al equipo

Aceptar la invitación al repositorio. Desde una carpeta local vacía ejecutar (el punto final evita crear una subcarpeta):

```bash
git clone https://github.com/NazarenoAc/ProyBC-Devlights.git .
```

Luego crear una rama siguiendo los pasos anteriores. No subir contraseñas, tokens ni archivos con credenciales.
