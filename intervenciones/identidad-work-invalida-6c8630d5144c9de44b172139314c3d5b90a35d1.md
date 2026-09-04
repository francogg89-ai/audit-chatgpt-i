# Intervención auditora — identidad WORK_SHA no resoluble

WORK_ID=revolutions-orchestra-ai
CARRIL=I

PERIMETRO_ULTIMA_MODIFICACION=CONSTITUCION

## Corte recibido

WORK_REPO=https://github.com/francogg89-ai/work-claude-i
WORK_SHA_CITADO=6c8630d5144c9de44b172139314c3d5b90a35d1

AUDIT_REPO=https://github.com/francogg89-ai/audit-chatgpt-i
AUDIT_SHA=fd356b9369cf5bd80a9a15a6695453f2e191dcfe

## Comprobación independiente

La identidad de work transportada no resuelve una entrega autoritativa:

- el valor citado tiene 39 caracteres, no 40;
- GitHub rechaza `6c8630d5144c9de44b172139314c3d5b90a35d1` como commit de `francogg89-ai/work-claude-i`;
- por lo tanto no puede aplicarse D1 sobre ese supuesto corte;
- tampoco puede inspeccionarse por identidad exacta el delta, el candidato, `verificacion-2/`, la salida literal, los insumos sintéticos ni la evidencia de la invocación abortada;
- en consecuencia no puede interpretarse todavía la corrida contra el contrato congelado.

Una búsqueda independiente de commits del repositorio muestra una entrega reciente con mensaje compatible con la acción esperada y una identidad textual muy próxima, pero esa identidad es distinta del valor transportado. El AUDITOR no la sustituye, no completa el SHA faltante y no la trata como el corte recibido.

## Autoridad aplicable

`ROL-AUDITOR.md` exige inspeccionar directamente el candidato y la evidencia en su identidad exacta; lo transportado es cita, no evidencia.

REVOLUTIONS conserva Git como autoridad y no habilita reparación semántica de identidades de transporte.

El precedente durable de este mismo carril para una identidad WORK_SHA de 39 caracteres resolvió el caso devolviendo al CONSTRUCTOR corriente para reemitir la identidad exacta ya publicada, sin modificar material ni crear un commit de corrección.

## Clasificación

DEFECTO=IDENTIDAD_DE_TRANSPORTE_INVALIDA
CLASE=METODOLOGICA
BLOQUEA_AUDITORIA_DE_U2=SI

No se pronuncia ningún veredicto sobre:

- la corrida con veredicto;
- F1/F6/F7;
- OBS-01;
- la invocación abortada previa;
- la condición de corrida única;
- el cierre o no de U2.

Esas materias requieren primero una identidad WORK_SHA exacta y resoluble.

## Veredicto

VEREDICTO=NO_AUDITABLE_POR_IDENTIDAD_INVALIDA

No se crea `auditorias/<WORK_SHA>.md` porque el valor recibido no identifica una entrega Git real. Esta intervención vive fuera de `auditorias/`.

## Próxima acción

PROXIMA_ACCION=El CONSTRUCTOR corriente debe obtener desde Git la identidad SHA completa y exacta de la entrega de U2 ya publicada que contiene la corrida bajo el contrato congelado, sin modificar REGLAS-ORQUESTADOR.md, EVENTO.md, verificacion-2/, verificador/ ni crear un nuevo commit por esta corrección de transporte, y reemitir el pase hacia AUDITOR con esa identidad válida. El AUDITOR recién entonces aplicará derivación e interpretará la corrida, incluida la invocación abortada previa, exclusivamente contra el contrato congelado.

DECISION_HUMANA_OBTENIDA=NINGUNA
