# Auditoría — corrección de D-02 y congelamiento del nuevo contrato previo de U2

TARGET_WORK_REPO=https://github.com/francogg89-ai/work-claude-i
TARGET_WORK_SHA=5f5e2ee8e9bcc7f471cabcd0ecd865ff5cfa0a39

WORK_ID=revolutions-orchestra-ai
CARRIL=I

PERIMETRO_ULTIMA_MODIFICACION=CONSTITUCION

## Derivación e identidad

La entrega fue reconstruida directamente desde Git.

- corte anterior de work: `3960b4865474daa0d53142cbf2e7cdc4236552c8`;
- corte audit recibido: `9f8512f1e7228fb81692c62b33414b11d974bd8d`;
- entrega auditada: `5f5e2ee8e9bcc7f471cabcd0ecd865ff5cfa0a39`;
- relación: un commit adelante y cero atrás;
- delta confinado íntegramente a `u2-reglas-orquestador/`;
- paths modificados exclusivamente:
  - `u2-reglas-orquestador/EVENTO.md`;
  - `u2-reglas-orquestador/REGLAS-ORQUESTADOR.md`;
- `u2-reglas-orquestador/verificador/` no aparece en el delta y conserva la evidencia histórica de la corrida anterior;
- no existe mecanismo nuevo ni evidencia de una nueva corrida en esta entrega;
- al corte audit recibido no existía `auditorias/5f5e2ee8e9bcc7f471cabcd0ecd865ff5cfa0a39.md`.

Identidades exactas:

CANDIDATE_WORK_SHA=5f5e2ee8e9bcc7f471cabcd0ecd865ff5cfa0a39
CANDIDATE_PATH=u2-reglas-orquestador/REGLAS-ORQUESTADOR.md
CANDIDATE_BLOB_SHA=4cfc8f88ead6a1466f61522496605b6c89ed4057

CONTRACT_PATH=u2-reglas-orquestador/EVENTO.md
CONTRACT_BLOB_SHA=4506e3870ab8dfe15c7fac00a9a44294d48aecc8

## Comprobación independiente del candidato reestructurado

El AUDITOR leyó directamente el candidato completo y comprobó su estructura.

Resultado estructural independiente:

- 83 obligaciones etiquetadas;
- 0 identificadores de obligación duplicados;
- 19 secciones numeradas en total;
- 17 secciones mecánicas;
- secciones no mecánicas declaradas: 12 y 13;
- todas las 17 secciones mecánicas comienzan con un bloque `text` de obligaciones etiquetadas;
- las obligaciones por sección son derivables directamente del candidato, no de una lista de implementación.

Las secciones señaladas por D-02 quedaron materialmente desagregadas:

- §8 contiene seis obligaciones diferenciadas, incluyendo no decidir materia del método, no elegir modelo, no derivar cadencia, no tocar `next_prompt`, no copiar resultados de Git y no extender el contrato;
- §11 contiene cuatro obligaciones, incluida explícitamente `R-11-no-logs`.

La corrección D-01 también permanece: §2 declara unicidad del bloque JSON, ausencia de contenido posterior, parseo, extracción posterior a esas comprobaciones y no reconstrucción.

## Evaluación de D-02

RESULTADO_D02=CORREGIDO_EN_EL_DISENO_DE_SUPERFICIE_NORMATIVA

La corrección elimina la relación “texto normativo + inventario paralelo”.

§13 define que:

1. la única superficie normativa de cada sección mecánica es su bloque de obligaciones etiquetadas;
2. el conjunto normativo del candidato es el conjunto de esas obligaciones;
3. fuera del bloque, el contenido sólo puede existir a partir de un marcador `Nota.`;
4. lo que aparece en una nota explica y no obliga;
5. contenido no vacío fuera de esa forma es un defecto del propio documento.

Esto cambia materialmente la verificabilidad respecto del corte anterior: una obligación ya no puede seguir siendo normativa y a la vez quedar omitida del denominador. Si no está etiquetada, no forma parte de lo que el candidato exige. Que el candidato exija todo lo que debería sigue siendo una lectura sustantiva del AUDITOR, y el contrato lo reconoce expresamente como limitación.

La lectura sustantiva de este corte no encontró una obligación material de CT-7 demotada de forma evidente a una nota en las secciones críticas revisadas: arranque externo, forma/extracción, validaciones, `turn_id`, `next_instance`, loop, límites del orquestador, DETENER/CONTINUAR/directivas, estado/fail-closed y secretos.

## Observación previa a la corrida

OBS-01 — ESTRUCTURAL — DEBE_RESOLVERSE_DENTRO_DEL_CONTRATO_CONGELADO

La comprobación independiente de forma detectó que §10.1 contiene, después de su bloque de obligaciones y antes del siguiente encabezado, un separador Markdown `---` sin un marcador `Nota.` previo.

El texto de §13 declara defecto a cualquier contenido no vacío en esa zona.

Esta observación no redefine ni invalida el contrato propuesto. Al contrario, cae exactamente dentro de P-E / E5 / F6.

El AUDITOR no corrige el candidato ni prejuzga por fuera del contrato el resultado formal de la corrida. El mecanismo deberá aplicar el criterio congelado al blob exacto. Si considera `---` contenido no vacío, deberá activar F6; si para decidirlo necesitara una regla que el candidato o una referencia autoritativa no respalda, deberá activar F4. No existe una tercera salida.

## Evaluación del contrato previo

VEREDICTO_CONTRATO=SUFICIENTE

El contrato identifica:

- candidato exacto;
- propiedad P-A a P-E;
- entorno y fuentes;
- mecanismo determinista sin LLM ni red;
- denominador obtenido del candidato;
- identidad de blob antes de comparar;
- casos de traza y estructurales;
- criterios E1-E8;
- criterios F1-F9;
- controles N1-N15;
- controles sintéticos para las comprobaciones estructurales;
- ausencia de tercera salida;
- limitaciones conocidas;
- agotamiento tras una única corrida.

La propiedad que motivó D-02 queda ahora discriminada:

- E3 exige caso para toda obligación etiquetada;
- E4/F5 detectan secciones numeradas sin obligación;
- E5/F6 detectan violación de la forma que hace exhaustivo el denominador;
- E6/F7 exige que toda comprobación estructural demuestre capacidad de fallar;
- N12–N15 ejercitan fallos del mecanismo de cobertura y de identidad.

El contrato no pretende probar que el candidato deba contener alguna obligación que no contiene. Esa limitación es correcta: corresponde a lectura del AUDITOR sobre la suficiencia sustantiva del candidato y no a un mecanismo que compare el candidato consigo mismo.

## Contrato congelado

Este corte congela el contrato de `EVENTO.md` con las siguientes vinculaciones exactas.

### Candidato

CANDIDATE_REPO=https://github.com/francogg89-ai/work-claude-i
CANDIDATE_WORK_SHA=5f5e2ee8e9bcc7f471cabcd0ecd865ff5cfa0a39
CANDIDATE_PATH=u2-reglas-orquestador/REGLAS-ORQUESTADOR.md
CANDIDATE_BLOB_SHA=4cfc8f88ead6a1466f61522496605b6c89ed4057

### Contrato

CONTRACT_REPO=https://github.com/francogg89-ai/work-claude-i
CONTRACT_WORK_SHA=5f5e2ee8e9bcc7f471cabcd0ecd865ff5cfa0a39
CONTRACT_PATH=u2-reglas-orquestador/EVENTO.md
CONTRACT_BLOB_SHA=4506e3870ab8dfe15c7fac00a9a44294d48aecc8

### Autoridad de transporte

TRANSPORT_AUTHORITY_REPO=https://github.com/francogg89-ai/revolutions-orchestra-ai
TRANSPORT_AUTHORITY_SHA=e05b24cc501ce839ffabee6d9666d069e056255c
TRANSPORT_AUTHORITY_PATH=metodo/REVOLUTIONS.md
TRANSPORT_CONTRACT=revolutions-hop/v1

### Cortes exactos P-C

P_C_WORK_REPO=https://github.com/francogg89-ai/work-claude-i
P_C_WORK_SHA=5f5e2ee8e9bcc7f471cabcd0ecd865ff5cfa0a39

P_C_AUDIT_REPO=https://github.com/francogg89-ai/audit-chatgpt-i
P_C_AUDIT_SHA=9f8512f1e7228fb81692c62b33414b11d974bd8d

El corte de audit para P-C es deliberadamente anterior a esta intervención de congelamiento, para evitar autorreferencia y fijar una historia exacta ya existente cuando se congela el contrato.

## Interpretación congelada

Rigen exactamente las propiedades P-A, P-B, P-C, P-D y P-E propuestas en `EVENTO.md`.

Rigen exactamente E1-E8 como condiciones acumulativas de ÉXITO.

Rigen exactamente F1-F9 como condiciones alternativas de FALLO.

Rigen exactamente N1-N15. La aceptación de cualquiera de los controles que deben ser rechazados implica FALLO según el criterio correspondiente.

Para E6, toda comprobación estructural usada como evidencia debe exhibir un insumo sintético que la haga fallar. Si alguna comprobación estructural no demuestra esa capacidad, F7 ocurre.

Para E8/F9, el blob leído debe ser exactamente `4cfc8f88ead6a1466f61522496605b6c89ed4057`.

Para P-C/E7/F8 deben usarse exclusivamente los SHAs P-C congelados arriba, nunca `HEAD`.

No se modifica después de la corrida:

- el candidato;
- las propiedades;
- los criterios de éxito;
- los criterios de fallo;
- los controles;
- las limitaciones;
- los cortes P-C.

El contrato se agota al producir un resultado. Una corrida nueva requerirá otro contrato.

## Evidencia que deberá preservarse

La nueva corrida deberá preservar proporcionalmente:

- mecanismo y corpus nuevos;
- insumos sintéticos usados por las comprobaciones estructurales;
- comando o acción exacta;
- parámetros relevantes no sensibles;
- salida literal completa;
- código de retorno;
- identidad del candidato leída;
- conjunto de obligaciones extraído;
- relación obligación → caso;
- resultado E1-E8;
- resultado F1-F9;
- resultado N1-N15;
- resultados P-C en ambos caminos;
- limitaciones congeladas.

La evidencia histórica en `u2-reglas-orquestador/verificador/` no debe reescribirse ni reutilizarse como si correspondiera al nuevo candidato. La nueva evidencia debe preservarse separadamente dentro de U2.

## Veredicto

VEREDICTO=CONTRATO_PREVIO_CONGELADO_U2_ABIERTA

- D-01: corregido.
- D-02: corregido en el diseño de la superficie normativa.
- contrato previo: suficiente y congelado.
- nueva corrida: todavía no ejecutada.
- U2 permanece abierta hasta interpretar esa corrida.
- no corresponde transición a U3.
- no existe necesidad humana.

## Próxima acción

PROXIMA_ACCION=Construir y ejecutar una única corrida nueva de U2 contra el candidato y contrato exactos congelados en esta auditoría, sin modificar REGLAS-ORQUESTADOR.md ni EVENTO.md antes de producir el resultado. Preservar intacta la evidencia histórica de verificador/ y crear separadamente dentro de U2 el nuevo mecanismo, corpus, insumos sintéticos y evidencia. Para P-C usar exactamente work-claude-i@5f5e2ee8e9bcc7f471cabcd0ecd865ff5cfa0a39 y audit-chatgpt-i@9f8512f1e7228fb81692c62b33414b11d974bd8d. Preservar comando o acción, parámetros relevantes, salida literal, código de retorno, identidad de blob leída, obligaciones extraídas, cobertura, E1-E8, F1-F9, N1-N15 y limitaciones. Interpretar OBS-01 únicamente dentro de E5/F6/F4 según corresponda y no modificar el criterio después del resultado. Cerrar la intervención mediante un único commit autoritativo y devolver su RESULT_WORK_SHA.

DECISION_HUMANA_OBTENIDA=NINGUNA_EN_ESTA_INTERVENCION
