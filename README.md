# RevistaFit

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.21949732.svg)](https://doi.org/10.5281/zenodo.21949732)

**Aplicación:** https://fborrasumh.github.io/revistafit/

Encuentra revistas para tu manuscrito **a partir de los artículos parecidos que ya se han publicado**. RevistaFit no adivina revistas: busca en OpenAlex los trabajos que más se parecen al tuyo y mira dónde se publicaron. Cada revista que propone viene con esos artículos como prueba y con datos comprobables: citación, acceso abierto, DOAJ y precio de publicación. Aplicación de un solo fichero (`index.html`), sin servidor.

## Novedades de la versión 2.0

- Recorrido guiado con el estilo de Forja: **Manuscrito → Lectura → Revistas**.
- **Funciona sin clave**: las búsquedas salen del título y de las palabras clave, y las revistas se ordenan con los datos de OpenAlex. Con clave (OpenAI o Ollama local), la IA lee el manuscrito, valora el encaje de cada revista y redacta la carta.
- **Búsquedas revisables** antes de lanzarlas, una por línea.
- **Revistas en español y portugués**: las búsquedas que empiezan por `[es]` o `[pt]` solo recuperan artículos en ese idioma, y las revistas se marcan con «publica en español/portugués».
- **Perfiles de prioridades** (Equilibrado, Que encaje, Máximo impacto, Abierto y barato), con los controles explicados.
- Distintivo **DOAJ**, país de la revista y aviso ante revistas de acceso abierto sin DOAJ y con poca trayectoria.
- **Exportación** de la lista en Markdown (con los artículos que sitúan a cada revista) y en CSV. La carta es editable, en Word, y en inglés, español o portugués.
- **Ejemplo que se prueba sin clave**, con búsqueda real en OpenAlex, y un segundo ejemplo en español.
- Modelo económico por defecto (gpt-6-luna) y clave compartida del catálogo (`ia_openai_key`).
- Corregido: una revista que la IA no llegaba a valorar contaba con encaje 0; ahora cuenta como neutra y se indica.

## Cómo ordena

| Prioridad | Origen del dato |
|---|---|
| Ajuste temático | Valoración de la IA (necesita clave) |
| Impacto citacional | Citación media a 2 años (OpenAlex) |
| Evidencia de encaje | Cuántos artículos parecidos al tuyo publicó la revista y en qué posición salían |
| Acceso abierto | OpenAlex y DOAJ |
| Coste asumible | Precio de publicación (APC) de lista |

## Lo que no hace

La citación media a 2 años de OpenAlex no es el factor de impacto del JCR ni sirve para acreditaciones. El APC es el de lista, sin descuentos por acuerdos institucionales. El tiempo de revisión no lo publica nadie de forma fiable, así que RevistaFit no lo inventa. Comprueba siempre el alcance, las normas y la indexación de la revista.

## Privacidad

El manuscrito se procesa en el navegador. Las búsquedas van a OpenAlex (datos CC0). Solo con clave, el texto viaja a OpenAI; con Ollama, se queda en el equipo. Las búsquedas se guardan en IndexedDB del navegador.

## Cómo citar

Borrás Rocher, F. (2026). *RevistaFit* (versión 2.0.0) [Software]. Universidad Miguel Hernández de Elche. https://doi.org/10.5281/zenodo.21949732

El DOI es el de concepto: apunta siempre a la última versión. GitHub ofrece la cita en APA y BibTeX con el botón *Cite this repository*, a partir de `CITATION.cff`.

Forma parte del catálogo [Herramientas IA para la academia](https://fborrasumh.github.io/ia/).

## Licencia

MIT © 2026 Fernando Borrás Rocher · Universidad Miguel Hernández de Elche.
