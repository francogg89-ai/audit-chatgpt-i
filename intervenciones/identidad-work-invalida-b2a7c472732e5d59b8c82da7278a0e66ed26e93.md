# Intervención auditora — identidad WORK_SHA no resoluble

WORK_ID=revolutions-orchestra-ai
CARRIL=I

PERIMETRO_ULTIMA_MODIFICACION=CONSTITUCION

## Corte recibido

WORK_REPO=https://github.com/francogg89-ai/work-claude-i
WORK_SHA_CITADO=b2a7c472732e5d59b8c82da7278a0e66ed26e93

AUDIT_REPO=https://github.com/francogg89-ai/audit-chatgpt-i
AUDIT_SHA=0ae8d8525c7ac0f6b84f547af44a1d00dfb59b03

## Comprobación independiente

La identidad de work transportada no puede localizar una entrega autoritativa:

- el valor citado tiene 39 caracteres, no 40;
- GitHub rechaza `b2a7c472732e5d59b8c82da7278a0e66ed26e93` como commit de `francogg89-ai/work-claude-i`;
- por lo tanto no puede ejecutarse D1 del protocolo de derivación sobre ese supuesto corte;
- tampoco puede inspeccionarse el candidato exacto ni congelarse un contrato previo asociado a esa identidad.

Una búsqueda independiente de commits del repositorio muestra una entrega reciente con texto y prefijo próximos, pero su identidad es distinta del valor transportado. No se la sustituye ni se la trata como evidencia del corte recibido.

## Autoridad aplicable

`ROL-CONSTRUCTOR.md` establece para turnos ordinarios que, si el prompt trae una identidad inexistente o la situación no resuelve inequívocamente, corresponde detenerse y devolver el problema en lugar de parchearlo.

`ROL-AUDITOR.md` exige inspeccionar el candidato en su identidad exacta y tratar lo transportado como cita, no como evidencia.

Por eso el AUDITOR no corrige, completa ni adivina el SHA.

## Clasificación

DEFECTO=IDENTIDAD_DE_TRANSPORTE_INVALIDA
CLASE=METODOLOGICA
BLOQUEA_AUDITORIA_DE_U2=SI

No es un defecto material de `REGLAS-ORQUESTADOR.md` ni del contrato previo propuesto: esos materiales no fueron auditados porque la identidad exacta que permitiría leerlos no fue transportada válidamente.

No existe todavía veredicto sobre la suficiencia del contrato previo de U2.

## Veredicto

VEREDICTO=NO_AUDITABLE_POR_IDENTIDAD_INVALIDA

No se crea `auditorias/<WORK_SHA>.md` porque el valor recibido no identifica una entrega Git y P8 aplica a auditorías de entregas reales.

## Próxima acción

PROXIMA_ACCION=El CONSTRUCTOR corriente debe obtener desde Git la identidad SHA completa y exacta de la entrega de U2 ya publicada, sin modificar material de U2 ni crear un nuevo commit por esta corrección de transporte, y reemitir el pase hacia AUDITOR con esa identidad válida. El AUDITOR recién entonces aplicará derivación, inspeccionará candidato y EVENTO.md y evaluará el contrato previo sin ejecutar ninguna mitad.

DECISION_HUMANA_OBTENIDA=NINGUNA
