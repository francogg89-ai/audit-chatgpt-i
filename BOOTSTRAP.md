# BOOTSTRAP — AUDITOR

## Constitución

WORK_ID=revolutions-orchestra-ai
CARRIL=I
ROL=AUDITOR

## Método gobernante

METHOD_REPO=https://github.com/francogg89-ai/revolutions-orchestra-ai
METHOD_SHA=e05b24cc501ce839ffabee6d9666d069e056255c

PATHS_CONSTITUTIVOS:
- metodo/REVOLUTIONS.md
- metodo/ROL-AUDITOR.md
- metodo/ROL-CONSTRUCTOR.md

ARCHIVOS_CARGADOS_POR_ESTE_ACTOR_AL_CONSTITUIR:
- metodo/REVOLUTIONS.md
- metodo/ROL-AUDITOR.md

METHOD_WRITE=PROHIBIDO

## Manifiesto de constitución

MANIFEST_REPO=https://github.com/francogg89-ai/manifiestos-trabajo-ai
MANIFEST_PATH=manifiestos/revolutions-orchestra-ai/MANIFIESTO_TRABAJO.md
MANIFEST_SHA=bb985e6580fbb8208f141a2af7646815bd1f7cdc

PROJECT=NO_APLICA

## Repositorios del loop

WORK_REPO=https://github.com/francogg89-ai/work-claude-i
AUDIT_REPO=https://github.com/francogg89-ai/audit-chatgpt-i

CONDICION_CONSTITUTIVA_WORK_REPO=VACIO
CONDICION_CONSTITUTIVA_AUDIT_REPO=VACIO

No existían WORK_SHA, AUDIT_SHA ni bootstrap previo al constituir este trabajo.

## Repositorios fuente y objeto

### manifiestos-trabajo-ai

REPO=https://github.com/francogg89-ai/manifiestos-trabajo-ai
FUNCION=biblioteca durable y repositorio que ya contiene el manifiesto aprobado
CORTE_CONSTITUTIVO=bb985e6580fbb8208f141a2af7646815bd1f7cdc

### reglas-orquestador-ai

REPO=https://github.com/francogg89-ai/reglas-orquestador-ai
FUNCION=objetivo del trabajo; construir las reglas mecánicas del orquestador
ESTADO_EN_CONSTITUCION=VACIO

### metodo-manifiestos-ai

REPO=https://github.com/francogg89-ai/metodo-manifiestos-ai
FUNCION=objetivo del trabajo; construir el método para constituir manifiestos
ESTADO_EN_CONSTITUCION=VACIO

### revolutions-orchestra-ai

REPO=https://github.com/francogg89-ai/revolutions-orchestra-ai
FUNCION=método autoritativo y fuente de sólo lectura
CORTE_CONSTITUTIVO=e05b24cc501ce839ffabee6d9666d069e056255c

## Raíz y paths locales del constructor

ROOT_LOCAL=C:\Franco_Metodos_AI

LOCAL_PATHS:
- WORK_REPO=C:\Franco_Metodos_AI\work-claude-i
- AUDIT_REPO=C:\Franco_Metodos_AI\audit-chatgpt-i
- MANIFEST_REPO=C:\Franco_Metodos_AI\manifiestos-trabajo-ai
- ORCHESTRATOR_RULES_REPO=C:\Franco_Metodos_AI\reglas-orquestador-ai
- MANIFEST_METHOD_REPO=C:\Franco_Metodos_AI\metodo-manifiestos-ai
- REVOLUTIONS_REPO=C:\Franco_Metodos_AI\revolutions-orchestra-ai

## Entornos relevantes

- GitHub remoto para las historias Git autoritativas.
- Windows local bajo C:\Franco_Metodos_AI para el trabajo del CONSTRUCTOR.
- No existe en esta constitución un entorno productivo externo que deba mutarse.
- No se transportan secretos.

## Capacidades inicialmente delegadas

### CONSTRUCTOR

ACTOR=CONSTRUCTOR
ENTORNO=GitHub remoto + Windows local bajo C:\Franco_Metodos_AI
CAPACIDADES:
- lectura de los repositorios fuente indicados;
- escritura exclusivamente en work-claude-i, conforme a ROL-CONSTRUCTOR;
- uso del filesystem y herramientas locales necesarias dentro de C:\Franco_Metodos_AI;
- ejecución de verificaciones técnicamente seguras dentro de ese perímetro;
- no escritura directa en audit-chatgpt-i;
- no escritura directa en metodo-manifiestos-ai, reglas-orquestador-ai, manifiestos-trabajo-ai ni revolutions-orchestra-ai.

### AUDITOR

ACTOR=AUDITOR
ENTORNO=GitHub remoto y fuentes disponibles
CAPACIDADES:
- lectura directa de work-claude-i y de todos los repositorios fuente indicados;
- escritura exclusivamente en audit-chatgpt-i, conforme a ROL-AUDITOR;
- comprobación independiente mediante GitHub y las fuentes disponibles;
- no modificación del candidato material;
- no escritura directa en metodo-manifiestos-ai, reglas-orquestador-ai ni manifiestos-trabajo-ai.

## Referencias seguras a credenciales

NINGUNA_REQUERIDA_AL_CONSTITUIR

## Fuentes auxiliares constitutivas

- No se constituye un repositorio de skills.
- metodo-lecciones-ai no es dependencia obligatoria de esta ejecución.
- La arquitectura resultante deberá dejar preparado, por exigencia del manifiesto, el punto de extensión futuro para repositorios auxiliares de lecciones, incidentes, experimentos y skills de sólo lectura, sin ampliar autoridad.

## Políticas iniciales de ejecución

- aplicar literalmente revolutions-orchestra-ai@e05b24cc501ce839ffabee6d9666d069e056255c;
- reconstruir desde Git y no desde memoria conversacional;
- no crear estado paralelo;
- no almacenar contadores vivos;
- no modificar el bootstrap para simular vigencia posterior de fuentes;
- no crear PROJECT.md por simetría: este trabajo no lo requiere;
- no crear EVENT.md central, lista viva de carriles ni registro redundante de mutaciones;
- los relevos de esta corrida son manuales o los que REVOLUTIONS requiera metodológicamente;
- no aplicar todavía una política periódica automática cada N;
- el diseño producido sí debe definir y verificar la política periódica requerida por el manifiesto;
- toda promoción fuera de work-* y audit-* debe respetar las fronteras estructurales de roles.

## Condición especial de bootstrap

metodo-manifiestos-ai y reglas-orquestador-ai son salidas de este mismo trabajo y estaban vacíos al constituir.

No se exige SHA previo de esos repositorios y no son autoridades gobernantes de esta ejecución.

El transporte de esta corrida se apoya directamente en el contrato definido por revolutions-orchestra-ai@e05b24cc501ce839ffabee6d9666d069e056255c.

Una vez publicados los tres repositorios nuevos, ejecuciones posteriores podrán congelar sus identidades Git exactas normalmente.

## Frontera de publicación final

El manifiesto exige que metodo-manifiestos-ai, reglas-orquestador-ai y manifiestos-trabajo-ai queden finalmente publicados.

CONSTRUCTOR y AUDITOR conservan sus fronteras estructurales de escritura. La promoción fuera de work-claude-i y audit-chatgpt-i deberá realizarse mediante una intervención externa compatible con REVOLUTIONS cuando corresponda; esta constitución no amplía capacidades de los roles.

## Cierre de la intervención constitutiva

PERIMETRO_ULTIMA_MODIFICACION=CONSTITUCION

PROXIMA_ACCION=Constituir al primer CONSTRUCTOR desde cero con next_instance=fresh, transportando estos hechos constitutivos y la identidad exacta de este BOOTSTRAP.md; no exigir bootstrap propio ni WORK_SHA previo inexistente.
