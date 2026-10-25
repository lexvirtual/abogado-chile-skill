# Abogado Chile ⚖️🇨🇱

> ⚠️ **Importante:** este skill entrega orientación legal y borradores, **no reemplaza a un abogado**. Antes de firmar, presentar un escrito o tomar una decisión, **consulta siempre con un abogado habilitado**. Si no puedes pagar uno, acude a la Corporación de Asistencia Judicial, la Defensoría Laboral, la Defensoría Penal Pública o una clínica jurídica universitaria.

Skill para asistentes de IA (Claude y Gemini) que actúa como **abogado experto en todo el derecho chileno**, en el ámbito público y privado.

Trabaja en dos fases:

1. **Explica tu caso**: qué está pasando, qué derechos tienes, qué ley lo regula, qué han dicho los tribunales y los organismos, riesgos y pasos a seguir, con **alerta de plazos**.
2. **Ofrece redactar el documento**: escrito, recurso de protección, descargos en sumario, presentación a Contraloría, reclamo a COMPIN o SUSESO, carta, correo, reclamo al SERNAC, borrador de demanda y más, con instrucciones de cómo presentarlo.

## Qué cubre

- **Áreas**: constitucional, civil, familia, laboral, seguridad social, penal, administrativo, tributario, comercial, consumidor, datos personales, libre competencia, propiedad intelectual, ambiental, urbanismo, recursos naturales, migración, indígena, electoral e internacional.
- **Organismos**: tribunales, Contraloría, Dirección del Trabajo, SUSESO, COMPIN, superintendencias (Salud, Pensiones, Educación, SEC, SISS), SII, SERNAC, CMF, Consejo para la Transparencia, municipios, SEA y SMA, INAPI, Migraciones, Fiscalía y Defensoría.
- **Fuentes oficiales**: LeyChile e Historia de la Ley (BCN), Cámara, Senado, Diario Oficial, Poder Judicial, Tribunal Constitucional, dictámenes de Contraloría, DT y SUSESO, entre otras.

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
1. Descarga la carpeta [`abogado-chile`](abogado-chile) y comprímela en un `.zip`.
2. En Claude, ve a **Configuración → Capacidades → Skills** y sube el `.zip`.

### Gemini
1. Descarga la carpeta [`abogado-chile`](abogado-chile).
2. En Gemini web, ve a **Configuración → Skills → Subir** y elige la carpeta (o el archivo `SKILL.md`).

### Claude Code
```bash
git clone https://github.com/lexvirtual/abogado-chile-skill.git
cp -r abogado-chile-skill/abogado-chile ~/.claude/skills/
```

## Uso

Cuenta tu caso con tus palabras. Para forzar el skill, escribe `/abogado-chile` al inicio:

```
/abogado-chile Trabajé 4 años en una empresa y ayer me despidieron por
"necesidades de la empresa". Me deben dos meses de cotizaciones.
```

Recibirás la explicación con normas, jurisprudencia, plazos y pasos, y al final un menú de documentos que puede redactar para ti.

## Aviso legal

Este skill **orienta, informa y redacta borradores**; no reemplaza la asesoría ni la representación de un abogado habilitado. Las respuestas de una IA pueden contener errores aunque se verifiquen las fuentes: revisa siempre los enlaces que entrega. Ante un juicio en curso, plazos por vencer, privación de libertad o montos relevantes, consulta a un abogado. Hay ayuda gratuita en la Corporación de Asistencia Judicial, la Defensoría Laboral, la Defensoría Penal Pública y las clínicas jurídicas universitarias.

## Contribuir

¿Encontraste un error o una norma desactualizada? Abre un *issue* o un *pull request*. Las correcciones con enlace a la fuente oficial son especialmente bienvenidas.

## Licencia

[MIT](LICENSE)
