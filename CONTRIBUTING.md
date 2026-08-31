# Cómo contribuir al sitio EL+MT

Este sitio está diseñado para que los profesores y colaboradores puedan
actualizar contenido sin modificar HTML, CSS ni la estructura del sitio.

## Qué archivos se pueden editar

El contenido se encuentra principalmente en:

- `_people/` — profesores y equipo
- `_research/` — áreas de investigación
- `_laboratories/` — laboratorios
- `_opportunities/` — tesis, proyectos, prácticas y convocatorias

Las plantillas se encuentran en:

- `templates/person.es.md`
- `templates/person.en.md`
- `templates/research.es.md`
- `templates/research.en.md`
- `templates/laboratory.es.md`
- `templates/laboratory.en.md`
- `templates/opportunity.es.md`
- `templates/opportunity.en.md`

## Qué archivos no se deben modificar

Salvo coordinación con los responsables del sitio, no modificar:

- `_layouts/`
- `_includes/`
- `assets/css/`
- `.github/workflows/`
- `_config.yml`

## Flujo recomendado

1. Crear una rama nueva.
2. Copiar la plantilla correspondiente.
3. Editar únicamente el contenido.
4. Hacer commit de los cambios.
5. Crear un Pull Request.
6. Después de la revisión y merge, GitHub Pages actualizará el sitio automáticamente.

## Ejemplo

Para añadir un profesor:

```bash
cp templates/person.es.md _people/nombre-apellido.es.md
