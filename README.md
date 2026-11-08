# SE 2026W – E3: Define Architecture and Design (Dronology)

UML models for exercise E3, written in PlantUML.

## Layout

| Path | Content |
|---|---|
| `class-diagramm.xml` | Original team class diagram (diagrams.net export) |
| `scN.puml`, `sc5.png`, `sc6.png` | Original sequence diagrams as handed in by each member |
| `reworked/class-diagram.puml` | Reworked class diagram, consistent with all sequence diagrams |
| `reworked/scN.puml` | Reworked sequence diagrams SC1–SC10. Messages are labelled with the dataset step numbers. A message marked `«SCn»` calls another scenario |
| `reworked/state-machine.puml` | UAV state machine, tied to SC1 Activate and Arm |

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

## Scenario calls

When one scenario includes another, it calls a method instead of drawing a `ref` box. The called diagram starts with that same method as an incoming message (`[-> Class : method()`), and the call is marked `«SCn»`.

| Called scenario | Method | Called from |
|---|---|---|
| SC7 Fly to Destination | `DroneResponse.requestFlightTo(destination)` | SC4 step 1, SC9 step 1 |
| SC8 Image Capture | `UAV.captureAndAnalyzeImagery()` | SC2 step 2, SC4 steps 2.1–2.2, SC9 step 4 |
| SC10 Lease Airspace | `UAV.triggerLease()` | SC5 step 4, SC7 step 7 |
