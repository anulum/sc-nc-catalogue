<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
SC-NC-CATALOGUE — repository foundation
-->

# Architecture

## Current executable surface

The checkout contains:
- repository validation tooling;
- dedicated tests;
- workflow definitions;
- native documentation.

No domain component of SC-NC Catalogue is implemented yet, and no code has moved here from SC-NeuroCore. The metadata keeps domain capabilities, claims and qualified record formats empty.

## Intended records

1. **Model descriptor:** A model's identity, family, state variables, parameters and literature source.
2. **Equation profile:** The equations of one model, with their variables, units and integration form.
3. **Factory:** How a model is built from its descriptor, parameters and numeric format.

## Ownership

**This project owns** the planned SC-NC Catalogue records and boundary rules.

**Owned elsewhere:**

| Responsibility | Owner |
|---|---|
| the shared data model | SC-NC Core |
| simulation and native lanes | SC-NC Engine |
| training and plasticity | SC-NC Learn |
| the public package, documentation and releases of the monolith | SC-NeuroCore |

## Interpretation

- **Models.** A catalogue entry describes a model and its reference behaviour; it is not a biological validation.
- **Moves.** Code arrives only through SC-NeuroCore's split import gate, unit by unit; a planned move is not a moved capability.

Read [the documentation architecture](docs/ARCHITECTURE.md) for the planned records, rules and schema identifiers.
