# Abogado Chile ⚖️🇨🇱

Conjunto de skills para asistentes de IA (Claude y Gemini) que actúan como **abogados expertos en derecho chileno**. Un skill general, **abogado-chile**, recibe el caso, lo clasifica y lo deriva a uno de **12 especialistas**.

Todos trabajan en dos fases:

1. **Explican tu caso**: qué pasa, qué derechos tienes, qué ley lo regula, qué han dicho tribunales y organismos, riesgos y pasos a seguir, con **alerta de plazos**.
2. **Ofrecen redactar el documento**: escrito, recurso, descargos, reclamo, carta o correo, con instrucciones de cómo presentarlo.

## Los skills

| Carpeta | Título | Qué cubre |
|---|---|---|
| [`abogado-chile`](abogado-chile) | Abogado Chile (recepción) | Todas las áreas; clasifica el caso y deriva al especialista |
| [`abogado-laboral-chile`](abogado-laboral-chile) | Abogado Laboral | Despidos, finiquitos, autodespido, nulidad del despido, tutela, Ley Karin, jornada de 42 horas |
| [`abogado-licencias-seguridad-social`](abogado-licencias-seguridad-social) | Licencias Médicas y Seguridad Social | COMPIN, SUSESO, isapres, Fonasa, Ley 16.744, AFP, reforma de pensiones |
| [`abogado-sumarios-funcionarios`](abogado-sumarios-funcionarios) | Sumarios y Funcionarios Públicos | Sumarios, investigaciones sumarias, descargos, contratas, reclamos ante Contraloría |
| [`abogado-familia-chile`](abogado-familia-chile) | Abogado de Familia | Alimentos y su cobro (Ley 21.484), cuidado personal, divorcio, VIF, mediación |
| [`abogado-consumidor-chile`](abogado-consumidor-chile) | Abogado del Consumidor | Garantía legal de 6 meses, retracto, SERNAC, Juzgado de Policía Local |
| [`abogado-civil-chile`](abogado-civil-chile) | Abogado Civil | Contratos, indemnizaciones, herencias, posesión efectiva, juicios civiles |
| [`abogado-arriendo-vivienda`](abogado-arriendo-vivienda) | Arriendo y Vivienda | Ley Devuélveme mi Casa, garantías, desalojo, copropiedad, compraventa |
| [`abogado-deudas-insolvencia`](abogado-deudas-insolvencia) | Deudas e Insolvencia | Prescripción, cobranza, embargos, Registro de Deuda Consolidada, renegociación |
| [`abogado-penal-chile`](abogado-penal-chile) | Abogado Penal | Víctimas e imputados, denuncia, querella, Defensoría de Víctimas (Ley 21.780) |
| [`abogado-tributario-chile`](abogado-tributario-chile) | Abogado Tributario | SII, citaciones, liquidaciones, RAV, reclamo ante TTA, honorarios |
| [`abogado-empresas-pymes`](abogado-empresas-pymes) | Empresas y Pymes | SpA, socios, contratos, cumplimiento, datos personales, insolvencia de empresas |
| [`abogado-ambiental-urbanismo`](abogado-ambiental-urbanismo) | Ambiental y Urbanismo | SEIA, SMA, tribunales ambientales, permisos de edificación (Ley 21.826) |

Se complementan con tres skills que ya existían: `abogada-derecho-administrativo-chile`, `solicitud-transparencia` y `datos-personales-21719`.

## Qué trae cada especialista

- Tabla de **datos verificados** en fuentes oficiales a octubre de 2026, con su norma o fuente.
- Lista de **datos que siempre hay que volver a verificar**, porque no se pudieron confirmar o cambian seguido.
- Procedimientos paso a paso y vías de reclamo.
- **Errores frecuentes** que hacen perder casos.
- **Checklist de documentos**.
- **Modelos de escritos** listos para adaptar.
- Ayuda gratuita disponible.

## Protocolo anti-error

Cada respuesta debe:

- Verificar cada ley en LeyChile, cada fallo en una fuente confiable y cada dictamen en el sitio del organismo.
- Marcar lo que no pudo confirmar: `[No verificado, confirmar en fuente oficial]`.
- Indicar si los plazos son hábiles o corridos y calcular la fecha límite.
- Confirmar el tribunal u organismo competente.
- Declarar un nivel de certeza (alto, medio o bajo).

> Requiere que el asistente tenga **búsqueda web activada**. Sin ella no puede verificar las fuentes.

## Instalación

### Claude (claude.ai o app de escritorio)
1. Descarga cada carpeta y comprímela en un `.zip` (o usa los `.zip` de la carpeta `para-claude`).
2. En Claude, ve a **Configuración → Capacidades → Skills** y sube cada `.zip`.
3. Instala primero `abogado-chile` y luego los especialistas que quieras.

### Gemini
1. Descarga las carpetas.
2. En Gemini web, ve a **Configuración → Skills → Subir** y elige cada carpeta (o su archivo `SKILL.md`).

### Claude Code
```bash
git clone https://github.com/manuvalenzu/abogado-chile-skill.git
cp -r abogado-chile-skill/abogado-* ~/.claude/skills/
```

## Uso

Cuenta tu caso con tus palabras. Para forzar el skill general, escribe `/abogado-chile` al inicio; para ir directo a un especialista, usa su nombre, por ejemplo `/abogado-laboral-chile`.

```
/abogado-chile Trabajé 4 años en una empresa y ayer me despidieron por
"necesidades de la empresa". Me deben dos meses de cotizaciones.
```

## Mantención

Las leyes cambian. Cada especialista indica la fecha de su última verificación (octubre de 2026). Al actualizar un dato, cambia la tabla de datos verificados y deja la fuente oficial.

## Aviso legal

Estos skills **orientan, informan y redactan borradores**; no reemplazan la asesoría ni la representación de un abogado habilitado. Las respuestas de una IA pueden contener errores aunque se verifiquen las fuentes: revisa siempre los enlaces que entrega. Ante un juicio en curso, plazos por vencer, privación de libertad o montos relevantes, consulta a un abogado. Hay ayuda gratuita en la Corporación de Asistencia Judicial (en transición al Servicio Nacional de Acceso a la Justicia, Ley 21.780), la Defensoría Laboral, la Defensoría Penal Pública y las clínicas jurídicas universitarias.

## Contribuir

¿Encontraste un error o una norma desactualizada? Abre un *issue* o un *pull request*. Las correcciones con enlace a la fuente oficial son especialmente bienvenidas.

## Licencia

[MIT](LICENSE)
