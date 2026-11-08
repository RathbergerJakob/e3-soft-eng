# SE 2026W – E3: Define Architecture and Design (Dronology)

UML models for exercise E3, written in PlantUML.

## Layout

| Path | Content |
|---|---|
| `class-diagramm.xml` | Original team class diagram (diagrams.net export) |
| `scN.puml`, `sc5.png`, `sc6.png` | Original sequence diagrams as handed in by each member |
| `reworked/class-diagram.puml` | Reworked class diagram, consistent with all sequence diagrams |
| `reworked/scN.puml` | Reworked sequence diagrams SC1–SC10. Messages are labelled with the dataset step numbers, and `ref` boxes mark where one scenario includes another |
| `reworked/notes` | Open review notes / TODOs |

## Scenario owners

| Member | Scenarios |
|---|---|
| lian_hsc | SC1, SC2 |
| Khan | SC3, SC4 |
| Tobi P | SC5, SC6 |
| Heidekraut | SC7, SC8 |
| Tiblue | SC9, SC10 |

## Consistency rule

Every message in a `reworked/scN.puml` must exist as an operation on the **receiving** class in `reworked/class-diagram.puml`.

## Scenario references (`ref`)

SC2→SC8, SC4→SC7, SC4→SC8, SC4→SC5, SC5→SC10, SC7→SC10, SC9→SC7, SC9→SC8
