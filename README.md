<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
SC-NC-CATALOGUE — repository foundation
-->

# SC-NC Catalogue

SC-NC Catalogue is being built as the catalogue of spiking neuron and synapse models split out of SC-NeuroCore: each model's descriptor, its equations and parameter profile, the factory that builds it, and the model profiles, reference traces and facet receipts that hold its behaviour to its source. It imports only SC-NC Core. This checkout contains repository validation tooling and documentation only. Full foundation qualification is in progress. There is no installed model catalogue, equation-profile checker, model factory or qualified record schema.

SC-NC Catalogue is part of the **SC Neuromorphic Computing Systems** group (SC-NEUROMORPHIC-COMPUTING-SYSTEMS). The [group and project map](https://github.com/anulum/sc-neurocore/blob/main/docs/ecosystem.md) shows the whole programme and where this repository sits in it.

**What does not exist yet:**
- any code moved from SC-NeuroCore;
- a registered runtime record schema;
- an installed model catalogue, equation-profile checker or model factory.

## Boundary

**What this project owns:**

| Record | Scope |
|---|---|
| Model descriptor | A model's identity, family, state variables, parameters and literature source |
| Equation profile | The equations of one model, with their variables, units and integration form |
| Factory | How a model is built from its descriptor, parameters and numeric format |

**Schemas it takes over from SC-NeuroCore:** sc-neurocore.model-profile (v1 and v2), sc-neurocore.reference-trace (v1 and v2) and sc-neurocore.facet-receipt (v1 and v2).

**Static imports:** only SC-NC Core.

**Records read without importing their code:** SC-NC Engine, SC-NC Data, SC-NC Analysis, SC-NC Compiler, SC-NC Learn, SC-NC Bridges, SC-NC Verify and Model Provenance Pack read this repository's records.

**Records it reads without importing their code:** those of SC-NC Core.

**Code planned to move here from SC-NeuroCore,** package by package, when SC-NeuroCore's split import gate allows it: `neurons`, `synapses`, `models`, `model_zoo`, `residual`, `spike_gnn` and `temporal_hierarchy`.

**Explicit non-claims and operating boundaries:**
- It contains no simulator, compiler or trainer; it describes models and builds them.
- A model's catalogue entry is not a claim that the model reproduces biology beyond its stated source and cases.

## Current tooling

Repository controls inspect:
- metadata and source attribution;
- workflows and dependency alignment;
- native documentation and repository inventory;
- preflight orchestration.

Metadata declares architecture-only maturity with empty implemented domain capability and claim inventories.

- Use the exact environment in [Contributing](CONTRIBUTING.md).
- Full CI and preflight belong in CI or in an explicitly admitted pre-push environment.
- See [Validation](VALIDATION.md) for the maintained validation scope.

## Intended evidence

Every future record will carry its source and environment digests, its numeric formats where it has them, and its explicit verification boundary. None of the planned record schemas is registered or qualified by this foundation.

## Documentation and support

Read [Architecture](ARCHITECTURE.md), [support](SUPPORT.md), [security reporting](SECURITY.md) and [citation metadata](CITATION.cff).

**Not claimed:**
- a hosted service, released package or DOI;
- a public CI status;
- a performed simulation, hardware measurement or benchmark result.

## Licence

Source is licensed under [AGPL-3.0-or-later](LICENSE). A commercial licence is available through the contact in [NOTICE](NOTICE.md).

![ANULUM](docs/assets/anulum_logo_company.jpg)

![Fortis Studio](docs/assets/fortis_studio_logo.jpg)

## Text and data mining reservation
The rightsholder, Miroslav Šotek (ANULUM), expressly reserves the use of the
works in this repository for text and data mining, including the collection of
this content for, and its use in, training, fine-tuning or evaluating machine
learning and artificial intelligence models, in accordance with Article 4(3) of
Directive (EU) 2019/790 and the national provisions transposing it.

No permission for such use has been granted beyond what the licence in
`LICENSE` grants. This reservation does not change that licence: uses the
licence permits remain permitted on its terms, including its attribution and
share-alike conditions.

Reservation made on 2026-11-22. Requests for permission: contact the
rightsholder through the contact listed in this repository.
