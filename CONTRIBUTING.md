# Guía de colaboración

Pasos que sigue cada integrante del grupo 213023_285 para aportar al proyecto Software FJ.

## 1. Obtener el código

Quien ya es colaborador del repositorio lo clona directamente. Quien no lo es puede hacer un fork y trabajar desde ahí.

```bash
git clone https://github.com/SecolDevs/programacion-grupo-213023_285.git
cd programacion-grupo-213023_285
```

## 2. Tomar un issue

Las tareas están en la pestaña Issues. Cada integrante trabaja los issues que tiene asignados y deja un comentario cuando empieza.

## 3. Crear una rama

Cada issue se resuelve en su propia rama, creada desde `main`.

```bash
git checkout main
git pull
git checkout -b docs/comentarios-cliente-servicios
```

El nombre de la rama empieza con el tipo de cambio.

| Prefijo | Uso |
| --- | --- |
| `feat/` | Código nuevo, como clases o simulaciones |
| `fix/` | Corrección de un error |
| `docs/` | Documentación y comentarios |

## 4. Probar antes de subir

Antes de cada commit se ejecuta el cuaderno completo con Restart and run all. La última celda debe mostrar que todas las simulaciones coinciden con lo esperado. Si el cambio toca el código, también se sube el archivo `software_fj.log` que deja esa ejecución.

## 5. Hacer commits descriptivos

El mensaje dice qué cambió, en presente y con el mismo prefijo de la rama.

```bash
git add Software_FJ_Fase4.ipynb software_fj.log
git commit -m "docs: comenta las validaciones de la clase Cliente"
git push -u origin docs/comentarios-cliente-servicios
```

## 6. Abrir el pull request

El pull request se abre contra `main` y su descripción incluye `Closes #N`, con el número del issue, para que se cierre al fusionar. Otro integrante lo revisa antes de fusionarlo.
