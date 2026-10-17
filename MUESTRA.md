# Quiver T-09 · Muestra de registro de decisiones

Autor: EazyHood, con asistencia de IA. Fuente fijada al commit `9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e`.

Muestra M0 de diez decisiones, en cuatro fases. No afirma asignación, aprobación, prueba física ni cumplimiento de M1/M2. La investigación enlaza cada afirmación a un pasaje concreto y conserva las incertidumbres.

## Criterio de estados

**Standing**: decisión sustentada en la fase citada, sin sustitución identificada dentro de esta muestra; no certifica el estado físico actual. **Superseded**: existe sustitución explícita citada. **Open**: queda una limitación o contradicción que impide cerrar su vigencia o resultado. Las fechas no documentadas no se inventan.

## Tabla de registro solicitada

| ID | Phase | Decision | Replaced | Why | Evidence | Status |
|---|---|---|---|---|---|---|
| D-001 | PT1 | Calcular CG e inercias desde el CAD de Onshape; actualizar una masa añadida con promedio ponderado y ejes paralelos. | No se identifica un método anterior. | Hacer repetible el cálculo sin esperar el cierre de todos los detalles del diseño. La nota propone un script Octave. | [Fuente 1](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/task-grant-bounty/pt1/avionics/0001-cg-inertia-matrix/information-note.md#L9-L24) | Open |
| D-002 | PT1 | Seleccionar el conjunto integrado Hobbywing XRotor X6 Plus. | Alternativas comparadas en la tabla; no consta una sustitución de hardware ya instalado. | La comparación del informe favorece coste, empuje y peso, además de reducir el trabajo de instalación. | [Fuente 1](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/docs/Engineering-Reports/PT1-Engineering-Report.md#L567-L591) | Open |
| D-003 | PT2 | Utilizar conectores EURO en la PCB principal. | No se identifica el conector previo a PT2. | Facilitar el mantenimiento, según la lista de capacidades de PT2. | [Fuente 1](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/docs/Engineering-Reports/PT2-Engineering-Report.md#L450-L464); [Fuente 2](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/docs/Engineering-Reports/PT3-Engineering-Report.md#L122-L124) | Superseded by D-005 |
| D-004 | PT2 | Separar la precarga al accionar el interruptor principal y la activación del SSR mediante radio y GPIO del controlador. | No se documenta una arquitectura anterior en este pasaje. | Limitar la corriente de irrupción antes del cierre del SSR; permitir cortar potencia a los motores desde el control remoto. | [Fuente 1](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/docs/Engineering-Reports/PT2-Engineering-Report.md#L470-L473); [Fuente 2](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/docs/Engineering-Reports/PT3-Engineering-Report.md#L126-L128) | Standing |
| D-005 | PT3 | Reemplazar terminales estilo Euro por conectores Phoenix en la PCB principal. | D-003: conectores EURO de PT2. | El informe justifica el cambio por prototipado más rápido y conexiones de campo más fiables. | [Fuente 1](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/docs/Engineering-Reports/PT3-Engineering-Report.md#L118-L128) | Standing |
| D-006 | PT3 | Situar GNSS aproximadamente 2 cm sobre el recinto FCU mediante un soporte de arco, separado de la PCB. | Se introduce un soporte nuevo; no se identifica aquí la ubicación exacta anterior. | Reducir interferencia electromagnética y sostener el receptor sin contacto directo con FCU/PCB. | [Fuente 1](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/task-grant-bounty/pt3/structural/0001-comprehensive_airframe_modification/information-note.md#L71-L78) | Open |
| D-007 | PT3 | Montar las interfaces de accesorios en extensores de 3 cm. | Se añade separación respecto al fuselaje; la nota no especifica todos los montajes anteriores. | Mejorar el acceso para desmontar y reemplazar equipos de misión. | [Fuente 1](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/task-grant-bounty/pt3/structural/0001-comprehensive_airframe_modification/information-note.md#L85-L93) | Standing |
| D-008 | PT3 | Prolongar los orificios de los tornillos inferiores de los brazos a través de las paredes de batería y añadir recortes de acceso. | Acceso previo entre placa intermedia y pared de batería mediante orificios achaflanados. | Los tornillos eran difíciles de sustituir; los recortes permiten utilizar una llave Allen. | [Fuente 1](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/task-grant-bounty/pt3/structural/0001-comprehensive_airframe_modification/information-note.md#L125-L129) | Standing |
| D-009 | Dev kit | Fijar la PCB principal a una interfaz impresa en 3D montada sobre amortiguadores de goma. | La nota no identifica un montaje anterior concreto. | Reducir la transmisión de vibración de alta frecuencia desde el bastidor a la PCB y sensores del controlador. | [Fuente 1](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/task-grant-bounty/Dev-Kit/PCB-Vibration-Mount.md#L1-L27) | Standing |
| D-010 | Dev kit | Documentar la maleta Pelican 1640 y espuma PE, manteniendo abierta la contradicción con Nanuk en la misma nota. | La propuesta incorporada dice Nanuk; el resumen de realización dice Pelican 1640. | Transportar el dron y accesorios con retención y protección. | [Fuente 1](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/task-grant-bounty/Dev-Kit/Transport-Case-Foam-Insert.md#L9-L27) | Open |

## D-001 · PT1 · Open

**Decisión:** Calcular CG e inercias desde el CAD de Onshape; actualizar una masa añadida con promedio ponderado y ejes paralelos.
**Sustituye:** No se identifica un método anterior.
**Motivo documentado:** Hacer repetible el cálculo sin esperar el cierre de todos los detalles del diseño. La nota propone un script Octave.
**Límite de la evidencia:** La fuente omite tornillería, cables y conectores. No extrapolar estos resultados a la masa medida del dev kit ni afirmar que aquí se validó el script.
**Evidencia:** [task-grant-bounty/pt1/avionics/0001-cg-inertia-matrix/information-note.md, líneas 9–24](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/task-grant-bounty/pt1/avionics/0001-cg-inertia-matrix/information-note.md#L9-L24)

## D-002 · PT1 · Open

**Decisión:** Seleccionar el conjunto integrado Hobbywing XRotor X6 Plus.
**Sustituye:** Alternativas comparadas en la tabla; no consta una sustitución de hardware ya instalado.
**Motivo documentado:** La comparación del informe favorece coste, empuje y peso, además de reducir el trabajo de instalación.
**Límite de la evidencia:** Selección histórica documentada. No confirma la variante ni el inventario de motores instalados en octubre de 2026.
**Evidencia:** [docs/Engineering-Reports/PT1-Engineering-Report.md, líneas 567–591](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/docs/Engineering-Reports/PT1-Engineering-Report.md#L567-L591)

## D-003 · PT2 · Superseded by D-005

**Decisión:** Utilizar conectores EURO en la PCB principal.
**Sustituye:** No se identifica el conector previo a PT2.
**Motivo documentado:** Facilitar el mantenimiento, según la lista de capacidades de PT2.
**Límite de la evidencia:** Sustituida explícitamente por Phoenix en PT3: véase D-005. No significa que toda placa PT2 haya sido retirada.
**Evidencia:** [docs/Engineering-Reports/PT2-Engineering-Report.md, líneas 450–464](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/docs/Engineering-Reports/PT2-Engineering-Report.md#L450-L464) · [docs/Engineering-Reports/PT3-Engineering-Report.md, líneas 122–124](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/docs/Engineering-Reports/PT3-Engineering-Report.md#L122-L124)

## D-004 · PT2 · Standing

**Decisión:** Separar la precarga al accionar el interruptor principal y la activación del SSR mediante radio y GPIO del controlador.
**Sustituye:** No se documenta una arquitectura anterior en este pasaje.
**Motivo documentado:** Limitar la corriente de irrupción antes del cierre del SSR; permitir cortar potencia a los motores desde el control remoto.
**Límite de la evidencia:** Arquitectura descrita, no ensayo propio de seguridad. El informe PT3 conserva precarga y control SSR; la implementación exacta requiere esquema de revisión.
**Evidencia:** [docs/Engineering-Reports/PT2-Engineering-Report.md, líneas 470–473](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/docs/Engineering-Reports/PT2-Engineering-Report.md#L470-L473) · [docs/Engineering-Reports/PT3-Engineering-Report.md, líneas 126–128](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/docs/Engineering-Reports/PT3-Engineering-Report.md#L126-L128)

## D-005 · PT3 · Standing

**Decisión:** Reemplazar terminales estilo Euro por conectores Phoenix en la PCB principal.
**Sustituye:** D-003: conectores EURO de PT2.
**Motivo documentado:** El informe justifica el cambio por prototipado más rápido y conexiones de campo más fiables.
**Límite de la evidencia:** El motivo se atribuye al informe; no se afirma una mejora de fiabilidad cuantificada por esta revisión.
**Evidencia:** [docs/Engineering-Reports/PT3-Engineering-Report.md, líneas 118–128](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/docs/Engineering-Reports/PT3-Engineering-Report.md#L118-L128)

## D-006 · PT3 · Open

**Decisión:** Situar GNSS aproximadamente 2 cm sobre el recinto FCU mediante un soporte de arco, separado de la PCB.
**Sustituye:** Se introduce un soporte nuevo; no se identifica aquí la ubicación exacta anterior.
**Motivo documentado:** Reducir interferencia electromagnética y sostener el receptor sin contacto directo con FCU/PCB.
**Límite de la evidencia:** Es intención del diseño. Faltan mediciones comparables de EMI para concluir que resolvió el problema.
**Evidencia:** [task-grant-bounty/pt3/structural/0001-comprehensive_airframe_modification/information-note.md, líneas 71–78](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/task-grant-bounty/pt3/structural/0001-comprehensive_airframe_modification/information-note.md#L71-L78)

## D-007 · PT3 · Standing

**Decisión:** Montar las interfaces de accesorios en extensores de 3 cm.
**Sustituye:** Se añade separación respecto al fuselaje; la nota no especifica todos los montajes anteriores.
**Motivo documentado:** Mejorar el acceso para desmontar y reemplazar equipos de misión.
**Límite de la evidencia:** Decisión dimensional explícita. No implica compatibilidad demostrada con todos los accesorios.
**Evidencia:** [task-grant-bounty/pt3/structural/0001-comprehensive_airframe_modification/information-note.md, líneas 85–93](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/task-grant-bounty/pt3/structural/0001-comprehensive_airframe_modification/information-note.md#L85-L93)

## D-008 · PT3 · Standing

**Decisión:** Prolongar los orificios de los tornillos inferiores de los brazos a través de las paredes de batería y añadir recortes de acceso.
**Sustituye:** Acceso previo entre placa intermedia y pared de batería mediante orificios achaflanados.
**Motivo documentado:** Los tornillos eran difíciles de sustituir; los recortes permiten utilizar una llave Allen.
**Límite de la evidencia:** Cambio de mantenibilidad documentado; no se ha cronometrado un montaje ni inspeccionado una unidad.
**Evidencia:** [task-grant-bounty/pt3/structural/0001-comprehensive_airframe_modification/information-note.md, líneas 125–129](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/task-grant-bounty/pt3/structural/0001-comprehensive_airframe_modification/information-note.md#L125-L129)

## D-009 · Dev kit · Standing

**Decisión:** Fijar la PCB principal a una interfaz impresa en 3D montada sobre amortiguadores de goma.
**Sustituye:** La nota no identifica un montaje anterior concreto.
**Motivo documentado:** Reducir la transmisión de vibración de alta frecuencia desde el bastidor a la PCB y sensores del controlador.
**Límite de la evidencia:** La fuente marca la nota Valid. No aporta aquí valores de atenuación medidos; se conserva como objetivo, no resultado certificado.
**Evidencia:** [task-grant-bounty/Dev-Kit/PCB-Vibration-Mount.md, líneas 1–27](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/task-grant-bounty/Dev-Kit/PCB-Vibration-Mount.md#L1-L27)

## D-010 · Dev kit · Open

**Decisión:** Documentar la maleta Pelican 1640 y espuma PE, manteniendo abierta la contradicción con Nanuk en la misma nota.
**Sustituye:** La propuesta incorporada dice Nanuk; el resumen de realización dice Pelican 1640.
**Motivo documentado:** Transportar el dron y accesorios con retención y protección.
**Límite de la evidencia:** La entrega no resuelve por inferencia la discrepancia. Pedir confirmación de modelo/BOM y marcar la propuesta antigua como sustituida si el responsable lo acredita.
**Evidencia:** [task-grant-bounty/Dev-Kit/Transport-Case-Foam-Insert.md, líneas 9–27](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/task-grant-bounty/Dev-Kit/Transport-Case-Foam-Insert.md#L9-L27)

## Preguntas que debe cerrar el responsable

1. ¿Qué revisión exacta de hardware, BOM y masa se considera el dev kit de referencia de 2026?
2. ¿Se confirma Pelican 1640 como realización final y Nanuk como propuesta sustituida?
3. ¿Quién facilita el pesaje del fuselaje, imágenes de construcción y datos solicitados por #209?
4. ¿Se confirma recompensa en efectivo/USDC y aceptación secuencial de M0, M1 y M2 antes de empezar el trabajo remunerado?
5. ¿Es admisible la documentación en español o se necesita traducción validada para M1/M2?

## Alcance que no se ha realizado

No se fabricó, pesó ni voló un dron. No se verificó la continuidad eléctrica ni se certificó seguridad operacional. No se adjudica retrospectivamente un motivo no escrito ni se presenta una simulación como medición. No se completa M1/M2 antes de la asignación.
