# Quiver T-09 · Decision-register sample

Prepared by EazyHood with AI assistance. Sources pinned to `9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e`.

M0 sample of ten decisions across four phases. It does not claim assignment, acceptance, physical testing, or completion of M1/M2. Each claim links to a specific passage and preserves uncertainty.

## Status definitions

**Standing** means supported in the cited phase, with no superseding decision found within this sample; it does not certify the current physical aircraft. **Superseded** identifies an explicitly cited replacement. **Open** preserves a limitation or contradiction that prevents closing the decision's current applicability or outcome. Undocumented dates are not invented.

## Requested register format

| ID | Phase | Decision | Replaced | Why | Evidence | Status |
|---|---|---|---|---|---|---|
| D-001 | PT1 | Calculate CG and inertia from Onshape CAD; incorporate an added mass using a weighted average and the parallel-axis theorem. | No earlier method is identified. | Make the calculation repeatable before all design details are finalized. The note proposes an Octave script. | [Source 1](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/task-grant-bounty/pt1/avionics/0001-cg-inertia-matrix/information-note.md#L9-L24) | Open |
| D-002 | PT1 | Select the integrated Hobbywing XRotor X6 Plus propulsion assembly. | Alternatives compared in the table; replacement of already-installed hardware is not established. | The report comparison favors cost, thrust, and weight, while reducing installation work. | [Source 1](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/docs/Engineering-Reports/PT1-Engineering-Report.md#L567-L591) | Open |
| D-003 | PT2 | Use EURO connectors on the main PCB. | The connector used before PT2 is not identified. | Improve maintainability, according to the PT2 feature list. | [Source 1](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/docs/Engineering-Reports/PT2-Engineering-Report.md#L450-L464); [Source 2](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/docs/Engineering-Reports/PT3-Engineering-Report.md#L122-L124) | Superseded by D-005 |
| D-004 | PT2 | Separate precharge triggered by the main switch from SSR activation through radio control and the flight controller GPIO. | No preceding architecture is documented in this passage. | Limit inrush current before the SSR closes, and allow motor power to be cut through remote control. | [Source 1](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/docs/Engineering-Reports/PT2-Engineering-Report.md#L470-L473); [Source 2](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/docs/Engineering-Reports/PT3-Engineering-Report.md#L126-L128) | Standing |
| D-005 | PT3 | Replace Euro-style terminals with Phoenix connectors on the main PCB. | D-003: PT2 EURO connectors. | The report attributes the change to faster prototyping and more reliable field connections. | [Source 1](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/docs/Engineering-Reports/PT3-Engineering-Report.md#L118-L128) | Standing |
| D-006 | PT3 | Position the GNSS approximately 2 cm above the FCU enclosure using an arch bracket, separated from the PCB. | A new bracket is introduced; the exact previous position is not identified here. | Reduce electromagnetic interference and support the receiver without direct contact with the FCU or PCB. | [Source 1](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/task-grant-bounty/pt3/structural/0001-comprehensive_airframe_modification/information-note.md#L71-L78) | Open |
| D-007 | PT3 | Mount attachment interfaces on 3 cm extenders. | Clearance from the airframe is added; the note does not specify every earlier mount. | Improve access when removing and replacing mission equipment. | [Source 1](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/task-grant-bounty/pt3/structural/0001-comprehensive_airframe_modification/information-note.md#L85-L93) | Standing |
| D-008 | PT3 | Extend the lower arm screw holes through the battery walls and add access cutouts. | Earlier access between the middle plate and battery wall through chamfered holes. | The screws were difficult to replace; the cutouts allow access with an Allen key. | [Source 1](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/task-grant-bounty/pt3/structural/0001-comprehensive_airframe_modification/information-note.md#L125-L129) | Standing |
| D-009 | Dev Kit | Secure the main PCB to a 3D-printed interface mounted on rubber dampers. | The note does not identify a specific earlier mount. | Reduce transmission of high-frequency vibration from the frame to the PCB and flight-controller sensors. | [Source 1](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/task-grant-bounty/Dev-Kit/PCB-Vibration-Mount.md#L1-L27) | Standing |
| D-010 | Dev Kit | Record the Pelican 1640 case and PE foam while leaving the contradictory Nanuk reference in the same note unresolved. | The embedded proposal names Nanuk; the implementation summary names Pelican 1640. | Transport the drone and accessories with retention and protection. | [Source 1](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/task-grant-bounty/Dev-Kit/Transport-Case-Foam-Insert.md#L9-L27) | Open |

## D-001 · PT1 · Open

**Decision:** Calculate CG and inertia from Onshape CAD; incorporate an added mass using a weighted average and the parallel-axis theorem.
**Replaced:** No earlier method is identified.
**Documented rationale:** Make the calculation repeatable before all design details are finalized. The note proposes an Octave script.
**Evidence limit:** The source omits fasteners, cables, and connectors. These results do not establish the measured mass of the dev kit, and this review did not validate the script.
**Evidence:** [task-grant-bounty/pt1/avionics/0001-cg-inertia-matrix/information-note.md, lines 9–24](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/task-grant-bounty/pt1/avionics/0001-cg-inertia-matrix/information-note.md#L9-L24)

## D-002 · PT1 · Open

**Decision:** Select the integrated Hobbywing XRotor X6 Plus propulsion assembly.
**Replaced:** Alternatives compared in the table; replacement of already-installed hardware is not established.
**Documented rationale:** The report comparison favors cost, thrust, and weight, while reducing installation work.
**Evidence limit:** This is a documented historical selection. It does not establish the exact variant or inventory installed in October 2026.
**Evidence:** [docs/Engineering-Reports/PT1-Engineering-Report.md, lines 567–591](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/docs/Engineering-Reports/PT1-Engineering-Report.md#L567-L591)

## D-003 · PT2 · Superseded by D-005

**Decision:** Use EURO connectors on the main PCB.
**Replaced:** The connector used before PT2 is not identified.
**Documented rationale:** Improve maintainability, according to the PT2 feature list.
**Evidence limit:** Explicitly superseded by Phoenix connectors in PT3: see D-005. This does not imply that every PT2 board was withdrawn.
**Evidence:** [docs/Engineering-Reports/PT2-Engineering-Report.md, lines 450–464](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/docs/Engineering-Reports/PT2-Engineering-Report.md#L450-L464) · [docs/Engineering-Reports/PT3-Engineering-Report.md, lines 122–124](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/docs/Engineering-Reports/PT3-Engineering-Report.md#L122-L124)

## D-004 · PT2 · Standing

**Decision:** Separate precharge triggered by the main switch from SSR activation through radio control and the flight controller GPIO.
**Replaced:** No preceding architecture is documented in this passage.
**Documented rationale:** Limit inrush current before the SSR closes, and allow motor power to be cut through remote control.
**Evidence limit:** This describes an architecture, not a safety test performed by this review. PT3 retains precharge and SSR control; the exact implementation requires the applicable schematic revision.
**Evidence:** [docs/Engineering-Reports/PT2-Engineering-Report.md, lines 470–473](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/docs/Engineering-Reports/PT2-Engineering-Report.md#L470-L473) · [docs/Engineering-Reports/PT3-Engineering-Report.md, lines 126–128](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/docs/Engineering-Reports/PT3-Engineering-Report.md#L126-L128)

## D-005 · PT3 · Standing

**Decision:** Replace Euro-style terminals with Phoenix connectors on the main PCB.
**Replaced:** D-003: PT2 EURO connectors.
**Documented rationale:** The report attributes the change to faster prototyping and more reliable field connections.
**Evidence limit:** The rationale is attributed to the report; this review does not claim a quantified reliability improvement.
**Evidence:** [docs/Engineering-Reports/PT3-Engineering-Report.md, lines 118–128](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/docs/Engineering-Reports/PT3-Engineering-Report.md#L118-L128)

## D-006 · PT3 · Open

**Decision:** Position the GNSS approximately 2 cm above the FCU enclosure using an arch bracket, separated from the PCB.
**Replaced:** A new bracket is introduced; the exact previous position is not identified here.
**Documented rationale:** Reduce electromagnetic interference and support the receiver without direct contact with the FCU or PCB.
**Evidence limit:** This is a design intention. Comparable EMI measurements are missing, so it cannot establish that the interference problem was resolved.
**Evidence:** [task-grant-bounty/pt3/structural/0001-comprehensive_airframe_modification/information-note.md, lines 71–78](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/task-grant-bounty/pt3/structural/0001-comprehensive_airframe_modification/information-note.md#L71-L78)

## D-007 · PT3 · Standing

**Decision:** Mount attachment interfaces on 3 cm extenders.
**Replaced:** Clearance from the airframe is added; the note does not specify every earlier mount.
**Documented rationale:** Improve access when removing and replacing mission equipment.
**Evidence limit:** The dimension is explicitly documented. It does not establish compatibility with every attachment.
**Evidence:** [task-grant-bounty/pt3/structural/0001-comprehensive_airframe_modification/information-note.md, lines 85–93](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/task-grant-bounty/pt3/structural/0001-comprehensive_airframe_modification/information-note.md#L85-L93)

## D-008 · PT3 · Standing

**Decision:** Extend the lower arm screw holes through the battery walls and add access cutouts.
**Replaced:** Earlier access between the middle plate and battery wall through chamfered holes.
**Documented rationale:** The screws were difficult to replace; the cutouts allow access with an Allen key.
**Evidence limit:** This is a documented maintainability change. No assembly time was measured and no physical unit was inspected during this review.
**Evidence:** [task-grant-bounty/pt3/structural/0001-comprehensive_airframe_modification/information-note.md, lines 125–129](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/task-grant-bounty/pt3/structural/0001-comprehensive_airframe_modification/information-note.md#L125-L129)

## D-009 · Dev Kit · Standing

**Decision:** Secure the main PCB to a 3D-printed interface mounted on rubber dampers.
**Replaced:** The note does not identify a specific earlier mount.
**Documented rationale:** Reduce transmission of high-frequency vibration from the frame to the PCB and flight-controller sensors.
**Evidence limit:** The source labels the note Valid. It provides no measured attenuation values here; vibration reduction remains an objective rather than a result certified by this review.
**Evidence:** [task-grant-bounty/Dev-Kit/PCB-Vibration-Mount.md, lines 1–27](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/task-grant-bounty/Dev-Kit/PCB-Vibration-Mount.md#L1-L27)

## D-010 · Dev Kit · Open

**Decision:** Record the Pelican 1640 case and PE foam while leaving the contradictory Nanuk reference in the same note unresolved.
**Replaced:** The embedded proposal names Nanuk; the implementation summary names Pelican 1640.
**Documented rationale:** Transport the drone and accessories with retention and protection.
**Evidence limit:** This submission does not resolve the discrepancy by inference. The model/BOM needs confirmation before the earlier proposal can be marked as superseded.
**Evidence:** [task-grant-bounty/Dev-Kit/Transport-Case-Foam-Insert.md, lines 9–27](https://github.com/Arrow-air/project-quiver/blob/9ef9efc80db1e0b7fa2fe03766c2bcf7a8eee03e/task-grant-bounty/Dev-Kit/Transport-Case-Foam-Insert.md#L9-L27)

## Questions for the project lead

1. Which exact hardware revision, BOM, and measured mass define the reference 2026 dev kit?
2. Is Pelican 1640 the final implementation and Nanuk the superseded proposal?
3. Who supplies the airframe weighing, build images, and weight data referenced by issue #209?
4. Can the payout currency and sequential acceptance of M0, M1, and M2 be confirmed before paid work starts?

## Work not performed

No drone was built, weighed, or flown. Electrical continuity and operational safety were not certified. Unwritten rationale is not assigned retrospectively, and simulation is not presented as measurement. M1/M2 have not been started before assignment.
