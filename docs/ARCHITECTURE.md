<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
SC-NC-CATALOGUE — repository foundation
-->

# Repository architecture

## Current executable tooling

**What it contains:** the repository's metadata, source-provenance, workflow, dependency-alignment, documentation, inventory and preflight controls.

**What each control does:** it inspects its fixed, declared local scope.

**What received metadata cannot do:** select another acceptance policy or grant domain authority.

Foundation qualification is in progress.

## Intended domain boundaries

| Record | Responsibility | Required evidence |
| --- | --- | --- |
| Model descriptor | A model's identity, family, state variables, parameters and literature source | Descriptor checks against the model's equations and declared parameter ranges |
| Equation profile | The equations of one model, with their variables, units and integration form | Equation and unit checks against the descriptor |
| Factory | How a model is built from its descriptor, parameters and numeric format | Every built model matches its descriptor and its reference trace |

## Planned record schemas

- `sc_nc_catalogue.model_descriptor.v1`
- `sc_nc_catalogue.equation_profile.v1`
- `sc_nc_catalogue.factory.v1`

These are planned identifiers. None of them is registered or qualified here.

It also takes over, unchanged, sc-neurocore.model-profile (v1 and v2), sc-neurocore.reference-trace (v1 and v2) and sc-neurocore.facet-receipt (v1 and v2) from SC-NeuroCore when their code moves here.

Read [validation tooling](validation-tooling.md) for the executable repository interfaces.
