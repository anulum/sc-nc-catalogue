<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
SC-NC-CATALOGUE — repository foundation
-->

# Decision: give SC-NC Catalogue its own repository in the SC-NeuroCore split

## Context

SC-NeuroCore holds every layer of the stack in one package, so a change to one layer can reach every other, and its import graph has cycles that no single layer can be qualified across. The split gives each layer its own repository, in an order in which a repository imports only those before it.

## Decision

**What SC-NC Catalogue owns:**
- model descriptor;
- equation profile;
- factory.

**What it imports:** SC-NC Core. Its records are read by SC-NC Engine, SC-NC Data, SC-NC Analysis, SC-NC Compiler, SC-NC Learn, SC-NC Bridges, SC-NC Verify and Model Provenance Pack, and it reads those of SC-NC Core.

**Owned elsewhere:**

| Responsibility | Owner |
|---|---|
| the shared data model | SC-NC Core |
| simulation and native lanes | SC-NC Engine |
| training and plasticity | SC-NC Learn |

## Consequences

**What can be qualified now:** repository governance and validation tooling, before any code moves here.

**What it cannot qualify:** unmoved code, unimplemented schemas or results.

**Architectural consequences:**
- code moves here only through SC-NeuroCore's split import gate, unit by unit, with its tests and language counterparts;
- SC-NC Catalogue never imports a repository later in the split order;
- SC-NeuroCore keeps a facade for each moved package until its users have moved.
