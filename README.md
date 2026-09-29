# GrantWriter

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.21423319.svg)](https://doi.org/10.5281/zenodo.21423319)

**Aplicación:** https://fborrasumh.github.io/grantwriter/

Redacta la memoria de tu proyecto de I+D+i para **CDTI, AEI, Horizonte Europa, IVACE, Torres Quevedo** u otras convocatorias. Nueve agentes buscan bibliografía real, se quedan solo con la pertinente, plantean la estrategia según los criterios de evaluación y redactan cada sección. **Lo que no les hayas contado lo dejan marcado para que lo completes tú.** Aplicación de un solo fichero (`index.html`), sin servidor.

## Novedades de la versión 2.0

- Recorrido guiado con el estilo de Forja: **Convocatoria → Proyecto → Secciones → Redacción → Memoria**.
- **Ejemplos**: una memoria de muestra que se ve sin clave (proyecto AEI de cribado de retinopatía con IA) y dos proyectos de prueba, uno académico y uno empresarial.
- **Nada inventado.** Los redactores no pueden inventar importes, socios, publicaciones, TRL ni valores de indicadores. Donde falta un dato escriben `[COMPLETAR: qué falta]`.
- **Comprobaciones deterministas** en la memoria:
  - datos por completar;
  - cifras que no aparecen en lo que aportó el usuario (se comparan números completos);
  - citas a referencias inexistentes;
  - contradicciones entre secciones.
- **Bibliografía pertinente.** Se busca en Semantic Scholar, OpenAlex, Europe PMC, PubMed, Crossref y arXiv, un agente lee los resúmenes para quedarse con los trabajos que sirven al proyecto, y solo se cita lo que el resumen respalda.
- **Corregido**: las mejoras del evaluador se aplicaban siempre a la primera sección; ahora cada una va a la sección que corresponde.
- **Secciones editables** y regenerables una a una. Las marcas se recalculan al guardar.
- **Exportación** a Word, Markdown, PDF (imprimir) o portapapeles. Las citas se renumeran por orden de aparición y la bibliografía incluye solo las citadas.
- La valoración con los criterios se presenta como lo que es: la opinión de un agente, no una predicción de la nota.
- La clave pasa a ser la compartida del catálogo (`ia_openai_key`); la de la versión 1 se migra sola. La sesión se guarda y se recupera.

## Los nueve agentes

| Fase | Agentes |
|---|---|
| Análisis y bibliografía | Analizador de contexto · Agente bibliográfico · Estado del arte |
| Estrategia y redacción | Estratega de la convocatoria · Redactor principal · Agente de impacto |
| Evaluación y ajuste | Adecuación a los criterios · Coherencia y mejoras · Control de calidad |

## Advertencia

Los criterios de cada convocatoria son orientativos: consulta siempre las bases oficiales del año y pega sus criterios. La memoria es un borrador que debes revisar, completar y firmar tú. Lee los trabajos que cites.

## Privacidad

Todo se procesa en el navegador. El texto viaja a OpenAI con la clave del usuario, guardada en `localStorage`. Las consultas bibliográficas van a las bases científicas citadas.

## Cómo citar

Borrás Rocher, F. (2026). *GrantWriter* (versión 2.0.0) [Software]. Universidad Miguel Hernández de Elche. https://doi.org/10.5281/zenodo.21423319

El DOI es el de concepto: apunta siempre a la última versión. GitHub ofrece la cita en APA y BibTeX con el botón *Cite this repository*, a partir de `CITATION.cff`.

Forma parte del catálogo [Herramientas IA para la academia](https://fborrasumh.github.io/ia/).

## Licencia

MIT © 2026 Fernando Borrás Rocher · Universidad Miguel Hernández de Elche.
