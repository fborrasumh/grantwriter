# GrantWriter

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.21423319.svg)](https://doi.org/10.5281/zenodo.21423319)

Borrador de la memoria de un proyecto de investigación para **cualquier convocatoria**, sin datos inventados. Aplicación web de un solo fichero (`index.html`), sin servidor.

**Usar la app:** https://fborrasumh.github.io/grantwriter/

**Idiomas:** español (por defecto), inglés y portugués; selector en la barra superior (o `?lang=en` / `?lang=pt` en la URL). La memoria puede redactarse en cualquiera de los tres, con independencia del idioma de la interfaz.

## Qué hace

1. **Tu proyecto** (una sola pantalla): nombre de la convocatoria, criterios de evaluación (si se dejan vacíos se usan tres genéricos: excelencia, impacto y calidad de la ejecución), título, descripción del proyecto (mínimo 60 palabras), equipo y datos disponibles, y documentos de apoyo opcionales (PDF, Word o texto, leídos en el navegador). Se eligen las secciones (seis por defecto, ocho posibles) y el idioma de la memoria.
2. **Redacción**: la IA propone tres búsquedas en inglés; la app consulta **OpenAlex** (todas las disciplinas), la IA se queda con los trabajos pertinentes (como mucho 10) y redacta cada sección por separado. Al final lee la memoria con los criterios y señala posibles contradicciones entre secciones. Son unas *n* + 3 llamadas a la IA para *n* secciones.
3. **La memoria**: se puede editar o rehacer cada sección y descargar en Word o Markdown, o copiar. Las citas se renumeran por orden de aparición y la bibliografía exportada lleva solo las referencias citadas, con su DOI.

Hay una **memoria de ejemplo** en los tres idiomas que se ve sin clave de IA.

## Qué comprueba el código (no la IA)

- **Datos por completar**: lo que la memoria necesita y no aportaste aparece como `[COMPLETAR: …]` (en inglés, `[COMPLETE: …]`) y se cuenta.
- **Cifras sin respaldo**: cada número del texto se busca en lo que escribiste, en tus documentos y en los resúmenes de la bibliografía; los que no aparecen se marcan en rojo (se ignoran años y el cronograma).
- **Citas inexistentes**: una cita `[N]` a un número que no está en la lista de referencias se marca en rojo.
- Las referencias salen de OpenAlex, no de la IA.

## Cómo se usa la IA

Con la clave propia de OpenAI, Google Gemini o Anthropic Claude, que se guarda solo en el navegador. La clave de OpenAI es la compartida del catálogo (`ia_openai_key`), así que quien usaba la versión 2 no tiene que volver a pegarla.

## Privacidad

El proyecto y la memoria se guardan en el navegador (IndexedDB). Al redactar, la información del proyecto sale hacia el proveedor de IA elegido con correos, teléfonos y DNI/NIE enmascarados; antes del primer envío de la sesión se muestra lo que sale y se pide confirmación. A OpenAlex solo van las tres búsquedas bibliográficas.

## Límites

- Es un **borrador**: hay que revisarlo, completarlo y firmarlo. Consulta siempre las bases oficiales de la convocatoria.
- La IA selecciona y cita bibliografía a partir del título y el resumen: **lee los trabajos que cites**. Que una cita apunte a una referencia existente no garantiza que la respalde.
- Las cifras «con respaldo» solo significan que el número aparece en tu material, no que esté bien usado.
- La lectura con los criterios es la opinión de la IA, sin nota; **no predice** la evaluación de la agencia.
- Los nombres propios no se enmascaran: no incluyas datos personales de terceros que no quieras enviar al proveedor.
- Probada con IA y OpenAlex simulados (flujo completo, marcas, exportaciones, idiomas, móvil); no se ha probado aquí con una clave real.

## Novedades de la versión 3.0

- Simplificada para cualquier investigador y cualquier convocatoria: dos pasos (proyecto y memoria) en lugar de cinco, sin plantillas de organismos concretos; se pegan los criterios de la convocatoria.
- Interfaz en español, inglés y portugués, y memoria en cualquiera de los tres.
- OpenAI, Google Gemini o Anthropic Claude, con desplegable de los modelos de la clave.
- Bibliografía de OpenAlex (antes, seis bases); menos llamadas a la IA.
- Aviso previo al envío con muestra y enmascarado de datos personales.
- Word generado en el navegador, sin librerías externas.

## Autoría

Fernando Borrás Rocher (Universidad Miguel Hernández de Elche). ORCID: [0000-0002-5519-4573](https://orcid.org/0000-0002-5519-4573)

## Cómo citar

Borrás Rocher, F. (2026). *GrantWriter* (versión 3.0.0) [Software]. Universidad Miguel Hernández de Elche. https://doi.org/10.5281/zenodo.21423319

El DOI es el de concepto: apunta siempre a la última versión. GitHub ofrece la cita en APA y BibTeX con el botón *Cite this repository*, a partir de `CITATION.cff`.

Forma parte del catálogo [Herramientas IA para la academia](https://fborrasumh.github.io/ia/).

## Licencia

MIT © 2026 Fernando Borrás Rocher · Universidad Miguel Hernández de Elche.
