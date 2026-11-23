# Adult VIS & VA-ECMO Shock Team Companion (Singapore Multi-Institution)

**Live GitHub Page:** https://lauyeehow1986-hub.github.io/vis/

An offline-capable, single-file (`index.html` / `adult_vis_calculator.html`) clinical calculator and Shock Team handoff aid designed for Singapore critical care units and acute hospital referrals.

## Formulas Implemented

### 1. Core VIS — Gaies et al. (2010) / AppCardio Equivalence
$$\text{VIS}_{\text{Core}} = \text{Dopamine} + \text{Dobutamine} + (100 \times \text{Adrenaline}) + (100 \times \text{Noradrenaline}_{\text{base}}) + (10 \times \text{Milrinone}) + (10{,}000 \times \text{Vasopressin}_{\text{U/kg/min}})$$

### 2. Full 13-Drug Extended Adult VIS — Belletti et al. (2021)
Adds all 7 extended agents alongside (while kept separate from) the Core 6-drug VIS:
- **Levosimendan** (`× 50` µg/kg/min)
- **Olprinone** (`× 25` µg/kg/min) — *greyed out: not registered on Singapore HSA Register of Therapeutic Products or National Drug Formulary (NDF); kept active for strict 13-drug Belletti 2021 parity / NPB / international transfers*
- **Methylene Blue** (`× 20` mg/kg/hr)
- **Phenylephrine** (`× 10` µg/kg/min)
- **Terlipressin** (`× 10` µg/min flat rate)
- **Angiotensin II** (`× 0.25` ng/kg/min)
- **Enoximone** (`× 1` µg/kg/min) — *greyed out: not registered on Singapore HSA Register of Therapeutic Products or NDF; kept active for strict 13-drug Belletti 2021 parity / NPB / international transfers*

## Singapore Multi-Institution Safety Features
- **Explicit Weight & Weight-Basis Confirmation:** Starts blank (no silent `70 kg` default) with `ABW` / `AdjBW` / `IBW` selector and blocks weight-dependent calculations until weight is provided.
- **Noradrenaline Base vs. Tartrate/Bitartrate Toggle:** Defaults to Singapore hospital **base (`1×`)** standard with an explicit **tartrate/bitartrate (`×0.5`)** equivalence mode per the 2024 SCCM/ESICM Task Force.
- **Unit Flexibility & Common SG Dilutions:** Per-drug selectors (`mcg/kg/min`, `mcg/min`, `mg/hr`, `mL/hr`, plus `U/hr` / `U/min` / `U/kg/min` for vasopressin) with one-click Singapore dilution presets.
- **Unit-Mismatch Plausibility Guardrails:** Flags common resuscitation entry errors (e.g., entering `0.04` in `U/hr` instead of `U/min` for vasopressin, or `> 2.0 mcg/kg/min` catecholamines).
- **Serial VIS-max Tracker & VA-ECMO Companion:** Session-only (`sessionStorage`) VIS trend log, shock phenotype mismatch warnings, ELSO 2021 / SCAI hypoperfusion & contraindication checklists, and PDPA-safe copyable SBAR output.

## Clinical Disclaimer
Decision-support aid only — **not** a standalone indication for VA-ECMO or substitute for multidisciplinary Shock Team judgment and institutional SOPs. Verify pump concentrations, weight basis, and noradrenaline base/salt labeling before clinical action.

## Primary References
- Gaies MG, et al. *Pediatr Crit Care Med*. 2010;11(2):234–238. (PMID 19794327)
- Belletti A, et al. *J Cardiothorac Vasc Anesth*. 2021;35(10):3067–3077. (PMID 33069558)
- Wieruszewski PM, Leone M, et al. *Crit Care Med*. 2024;52(4):521–530. (PMID 38240498)
- Na SJ, et al. *Rev Esp Cardiol*. 2019;72(1):40–47. (PMID 29463462)
- Lorusso R, et al. *ASAIO J*. 2021;67(8):827–844. (PMID 34339398)
- Hyun J, et al. *Circ J*. 2022;86(4):687–694. (PMID 34759121)
- Thiele H, et al. *N Engl J Med*. 2023;389:1286–1297. (PMID 37634145)
- Hu Y, et al. *J Thorac Dis*. 2024;16(2):1097–1107. (PMID 38505065)
- Caruso V, et al. *J Cardiothorac Vasc Anesth*. 2024;38(3):724–730. (PMID 38182434)
