# Flujo combinado para la tesis: claude-scientific-writer + thesis-writer

## Reparto de funciones

- **claude-scientific-writer**: investigación profunda, búsqueda de literatura real, verificación de citas, rigor científico, reporting guidelines y generación de documentos académicos.
- **thesis-writer** (`~/.claude/skills/thesis-writer`): estructura de capítulos, reglas por capítulo (`references/chapter-rules.md`), escaneo y corrección de los patrones de escritura de IA (`references/ai-patterns.md`, `scripts/ai_scan.py`), scoring de naturalidad y preparación de viva (`references/viva-questions.md`).

## Orden de trabajo al escribir o revisar un capítulo

1. **Rigor y citas (scientific-writer).** Buscar y verificar la literatura. Toda cita debe corresponder a un artículo real indexado en PubMed, preferentemente de revistas Q1 y alto factor de impacto. Si una cita no se puede verificar, marcarla `[CITATION NEEDED]`; nunca inventarla.
2. **Estructura (thesis-writer, Mode 1).** Redactar siguiendo `chapter-rules.md` si es un capítulo completo (regla de dos fuentes por párrafo, comparar en vez de describir, objetivos del Cap. 1 = secciones de resultados, un término por concepto).
3. **Scan + Fix (thesis-writer, Modes 2 y 3).** Pasar el texto por el escáner de patrones de IA, revisar los hallazgos en contexto (descartar falsos positivos) y reescribir solo los confirmados, sin perder ni alterar ninguna cita.
4. **Comprobación final.** Confirmar que el fix no cambió datos, citas ni hedging científico, y entregar: texto, resultado del scan, lista de citas con estado de verificación y riesgo de examinador.

## Reglas permanentes

- Nunca alucinar ni inventar información, referencias, datos o DOIs.
- Búsquedas bibliográficas: papers en PubMed, revistas Q1 y alto factor de impacto.
- Las correcciones de estilo (thesis-writer) nunca prevalecen sobre la exactitud científica (scientific-writer).
