---
type: Review
title: "MO§ES™ Framework — Adversarial Architecture Review and Hardening Plan v0.1"
description: "Adversarial review of the proposed canonical ontology, intelligence taxonomy, provenance discipline, and claims infrastructure for the MO§ES™ framework. Covers architecture review, canonical ontology v0.1, claims registry v0.1, prior-art/collision registry v0.1, formalization gaps, repository implementation recommendations, and six-perspective red-team attacks."
tags: [ontology, provenance, commitment-theory, intelligence-taxonomy, adversarial-review, canonical, moses]
timestamp: 2026-08-20
last_touched: 2026-08-20
---

# MO§ES™ Framework — Adversarial Architecture Review and Hardening Plan v0.1

**Author of review:** Devin (GTM session, operating in review/proposal mode)
**Owner of framework:** Deric J. McHenry / Ello Cello LLC
**Date:** 2026-08-20
**Status:** PROPOSAL — not canonical. No canonical Commitment Theory material has been modified. The Search Authority canon repository was unavailable (`~/Developer/active/search-authority` not found); this review uses existing public DOI-backed records as provenance anchors and explicitly flags where canonical confirmation is needed.

**Objective restated:** The objective is not to validate the framework. The objective is to make it difficult to fool ourselves.

---

## Provenance Anchors Used in This Review

| Artifact | DOI / Path | Authority |
|----------|-----------|-----------|
| Conservation Law paper v05 | `10.5281/zenodo.20029607` | Public, DOI-backed |
| Experimental record (EXP-001–007) | `10.5281/zenodo.19105225` | Public, DOI-backed |
| Transformation harness | `10.5281/zenodo.19109397` | Public, DOI-backed |
| Propositions prospectus P-000 | `10.5281/zenodo.20031715` | Public, DOI-backed |
| Concept DOI | `10.5281/zenodo.18267278` | Public, DOI-backed |
| Commitment Theory repo | `commit_theory/Commitment_Theory/` | Local, canonical |
| Conservation Law repo | `commit_theory/Commitment_Conservation/` | Local, canonical |
| CIVITAE ontology | `built/agent-universe/ONTOLOGY.md` | Local, establishes AAI/BI priority |
| Enterprise build package | `active/b2bpilot/ENTERPRISE_BUILD_PACKAGE_2026-08-17/` | Local, enterprise |
| Naming architecture | `CT/workspace/naming-architecture/` | Local, canonical |
| Competition analysis | `CT/workspace/COMPETITION_ANALYSIS.md` | Local, internal lead |
| Provisional patent | Serial No. 63/877,177 | Filed |

**Governance blocker:** The Search Authority canon repository (`~/Developer/active/search-authority`) was not found. Per governance rules, canonical context must not be invented when the canon is unavailable. This review is therefore framed as a **proposal/review**, not as canonical edits. Any canonical changes require owner clarification or discovery of the actual canon location.

---

## Deliverable A — Architecture Review

### A.1 What Holds

**A.1.1 The Conservation Law has a genuine empirical anchor.**
The existing Commitment Theory work is not merely conceptual. It has DOI-backed publications, seven controlled experiments (EXP-001 through EXP-007, 3,950 total run entries), a public falsification protocol with pinned transformation suite and observable, and a versioned harness. The 0.94 vs. 0.42 stability separation across enforced and unenforced regimes is a real empirical signal, even if the corpus is small (100 sentences, 50 code snippets, 25 proofs). This is more empirical grounding than most philosophical frameworks possess.

**A.1.2 The falsification protocol is structurally sound.**
The pinned contract (Section 4 of the v05 paper) specifies a representative transformation suite, a publicly computable observable (min-aggregated Jaccard + cosine + NLI), explicit refutation conditions, and attractor rejection. The Goodhart resistance design (min-aggregation, swappable oracle, lineage DAG) addresses the most obvious gaming attacks. The protocol invites third-party replication with public components only.

**A.1.3 The deontic focus is genuinely distinguishing.**
The existing disambiguation work (Disambiguation_Guide.md) correctly distinguishes CT's commitment from Brandom's discursive commitment (agent-side vs. signal-side), Walton & Krabbe's commitment stores (diachronic dialogue vs. synchronic signal), CommitmentBank (speaker factuality vs. deontic preservation), cryptographic commitment (protocol vs. protected content), and organizational commitment (psychological bond vs. semantic invariant). These distinctions are real and defensible.

**A.1.4 The naming architecture resolved a real collision.**
The CCT → CT rename was motivated by a genuine search collision with Hobfoll's Conservation of Resources theory (19,000+ citations, 35 years of institutional weight). The fix — "Conservation" stays at the law level, removed from the theory name — is clean. The nine novel concepts (commitment kernel, governed transformation, etc.) were verified as zero-collision as of April 2026.

**A.1.5 AAI/BI have existing internal priority.**
The CIVITAE ontology (`built/agent-universe/ONTOLOGY.md`) already classifies agents as AAI (AI Assisted Intelligence — silicon-side, powered by a System) or BI (Biological Intelligence — human-side, operating directly). This is established internal terminology that predates the current ontology proposal. Any new taxonomy must preserve this existing priority, not overwrite it.

### A.2 What Fails (or Is Not Yet Established)

**A.2.1 The conservation claim's formal status is ambiguous between definition and empirical law.**
The v05 paper's Section 3.4 ("Non-Tautology Clarification") acknowledges this objection directly: if commitment is defined as what survives identity-preserving transformation, conservation follows by construction. The paper's response — that the compression gate does not have prior access to C(S) and that conservation is therefore empirical — is structurally correct but only partially convincing. The issue is that the identity relation ~ (equivalence oracle) is also chosen by the framework. If ~ is defined to make conservation true, the claim is tautological; if ~ is independent, conservation is empirical. The paper parameterizes by ~ and invites critics to substitute stronger oracles, which is the right move, but the formal status depends entirely on whether ~ is genuinely independent of the commitment extractor C(.). This is the deepest unresolved issue in the existing framework, and it carries forward into the intelligence ontology extension.

**A.2.2 The proxy measurement gap is acknowledged but not closed.**
EXP-007 (NP-negation probe) confirmed that Jaccard blindness and lexical scope widening are real measurement failures. The paper distinguishes "surface-level extractor failure" from "semantic conservation failure," but this distinction is currently asserted rather than demonstrated. The claim that "apparent loss at the proxy layer does not necessarily imply disappearance of the underlying commitment itself" is unfalsifiable as stated — there is no independent way to check whether commitment persists when all proxies fail. This is a genuine measurement gap, not merely an implementation detail.

**A.2.3 The corpus is too small to support the strength of the conservation claim.**
100 sentences, 50 code snippets, 25 proofs, and 3,950 run entries are sufficient for proof-of-concept but not for the claim that conservation is a "foundational principle for language systems analogous to conservation laws in physics." The paper acknowledges this ("should be read as proof-of-concept rather than validation at scale") but the framing in abstracts and conclusions sometimes exceeds what the evidence supports. The competition analysis correctly identifies that large-scale adversarial replication is the critical next step.

**A.2.4 The BI/AAI/SI taxonomy has no operational criteria yet.**
The proposed intelligence classes (BI, AAI, SI) are currently labels without measurement procedures. The user's provisional definition of AAI — "intelligent operation requiring an originating external condition/event/intelligence rather than endogenous initiation" — is conceptually interesting but operationally undefined:
- What counts as "originating external condition"?
- How is "endogenous initiation" detected and distinguished from stimulus-response?
- Is a human prompted by another human AAI or BI?
- Is an LLM generating text in response to a prompt AAI or SI?
- Is a biological organism whose behavior is entirely stimulus-driven AAI or BI?

Without operational criteria, the taxonomy cannot be tested and risks becoming metaphysical furniture.

**A.2.5 The relational thesis BI × AAI → SI has no falsification condition.**
The thesis that biological intelligence combined with assisted intelligence produces system intelligence is currently stated as a conceptual claim, not a testable hypothesis. What observation would falsify it? What does "×" mean operationally — composition, interaction, emergence, causal production? Without specifying the operation and the falsification condition, the thesis cannot enter the claims registry as anything stronger than SPECULATIVE.

**A.2.6 Intelligence Provenance is proposed but not yet distinguished from existing provenance systems.**
The candidate provenance relations (originated_by, initiated_by, received_from, transformed_by, curated_by, redirected_by, authorized_by, committed_by, derived_from) overlap substantially with W3C PROV, data provenance, content provenance (C2PA), and model attribution systems. The distinguishing claim — that Intelligence Provenance traces intelligence itself, not just data or content — requires a definition of what "intelligence" is at the provenance level. If intelligence is treated operationally (as observable intelligence-bearing events), the provenance system may collapse into event provenance with an "intelligence" label. If intelligence is treated metaphysically, the system inherits all the unresolved problems of defining intelligence.

**A.2.7 The Micro Eval tuple is not yet derived from the ontology.**
The candidate representation Eμ = (Ia, St, T, Ib, St+1, C, P, O) is proposed as a measurement unit, but its relationship to the ontology is unclear. Are Ia and Ib participants, intelligence types, or intelligence-bearing events? Is C the commitment kernel from Commitment Theory, or a different commitment? Is P the provenance graph or a single provenance assertion? Without derivation from the ontology, the Micro Eval risks becoming a parallel conceptual system — exactly what the user warned against.

### A.3 What Remains Unresolved

**A.3.1 Is SI a participant class, an emergent property, a system state, or a separate construct?**
This is the central ontological question. Four possibilities:
1. **Participant class:** SI is a peer of BI and AAI, a thing that can initiate, transform, and bear commitment. This requires SI to have identity and agency.
2. **Emergent property:** SI is what arises when BI and AAI interact under certain conditions. It is not a participant but a property of the interaction. This is more parsimonious but makes "SI initiated_by X" ill-formed.
3. **System state:** SI is a state of a system that contains BI and AAI participants. It describes the system's configuration, not a new entity.
4. **Separate construct:** SI is a distinct ontological category that does not reduce to BI, AAI, or their interaction. This is the strongest claim and the hardest to defend.

**Recommendation:** Treat SI initially as an emergent property or system state (options 2 or 3), not as a participant class. This is the most parsimonious position and avoids premature metaphysical commitments. The taxonomy can be upgraded to option 1 or 4 if and only if operational criteria for SI-as-participant are developed and tested.

**A.3.2 Can Intelligence Provenance be rigorous without solving the metaphysics of intelligence?**
Yes, conditionally. The provenance system can be rigorous if it traces observable intelligence-bearing events (initiations, transformations, contributions, commitments, outcomes) rather than "intelligence" as a substance. This is the same move Commitment Theory makes with commitment: define it operationally as what the extractor extracts, not metaphysically as what commitment "really is." The risk is that operational definitions inherit the limitations of their measurement instruments (the proxy measurement gap, A.2.2).

**A.3.3 How do Commitment Theory and Intelligence Provenance connect formally?**
The connection is currently conceptual, not formal. The proposed bridge: commitment C(S) is an invariant that can be traced across provenance edges. If a signal S is transformed by T and the provenance edge records the transformation, then the commitment invariant C(S) = C(T(S)) (under governed transformation) is a property that can be checked at each provenance node. This makes the Conservation Law a constraint on the provenance graph, not a separate claim.

This is promising but requires:
- A formal specification of how C(S) is computed at each provenance node
- A definition of what happens when C(S) ≠ C(T(S)) (provenance edge is marked as commitment-violating)
- A distinction between commitment-preserving and commitment-violating provenance edges
- A way to handle the case where the commitment extractor itself changes across the provenance graph

**A.3.4 How do Micro Evals derive from the ontology rather than becoming a parallel system?**
The Micro Eval should be an instantiation of the ontology's measurement model, not a separate tuple. Specifically:
- Ia and Ib should be participants (instances of BI, AAI, or SI-as-property) from the ontology
- St and St+1 should be states from the ontology
- T should be a transformation from the ontology (governed or ungoverned)
- C should be the commitment kernel from Commitment Theory
- P should be a provenance subgraph from Intelligence Provenance
- O should be an observation from the measurement model

If these mappings are explicit, the Micro Eval is derived. If they are left implicit, the Micro Eval becomes a parallel ontology.

### A.4 Undefined Primitives

| Primitive | Status | Risk |
|-----------|--------|------|
| Signal | Defined in v05 paper (Section 2.1) | Low — existing definition is adequate |
| Transformation | Defined in v05 paper (Section 2.1) | Low |
| Commitment C(S) | Defined in v05 paper (Definition 2.4) and Naming_Architecture.md | Medium — definition depends on choice of extractor and equivalence oracle |
| Intelligence (I) | UNDEFINED | High — the most important undefined primitive in the proposed extension |
| Biological Intelligence (BI) | Provisionally defined as "human-side, operating directly" (CIVITAE) | Medium — "operating directly" is unclear |
| Assisted Intelligence (AAI) | Provisionally defined as "requires originating external condition to initiate" | High — "originating external condition" is undefined |
| System Intelligence (SI) | UNDEFINED | High — no operational definition exists |
| Initiation | UNDEFINED | High — must be distinguished from causation, prompting, control, dependency |
| Authority | Referenced in provenance relations but undefined | Medium |
| Curation | Referenced in provenance relations but undefined | Medium |

### A.5 Circular Definitions (Risk Assessment)

| Definition | Circularity Risk | Assessment |
|-----------|-----------------|------------|
| Commitment = "minimal identity-preserving content" | Identity-preserving = "preserves commitment" | REAL but acknowledged in v05 paper Section 3.4. Mitigated by parameterizing the equivalence oracle. |
| AAI = "requires external initiation" + Initiation = "what AAI requires" | Potential circularity if initiation is defined in terms of AAI | AVOIDABLE — define initiation independently (see Formalization Gaps) |
| SI = "emerges from BI × AAI" + BI × AAI = "what produces SI" | Potential circularity if the relational thesis is the only definition of both SI and the operation | AVOIDABLE — define the operation independently of the outcome |
| Intelligence Provenance = "traces intelligence" + Intelligence = "what provenance traces" | Potential circularity if intelligence is defined only as the object of provenance | AVOIDABLE — define intelligence operationally via observable events |

### A.6 Category Errors (Risk Assessment)

| Potential Error | Assessment |
|----------------|------------|
| Treating SI as a participant when it is an emergent property | HIGH RISK — the provenance relations (initiated_by, committed_by) presuppose an agent. If SI is emergent, these relations need reformulation. |
| Treating commitment as a property of agents rather than signals | LOW RISK — the existing framework is clear that commitment is signal-side. Must be preserved. |
| Treating provenance edges as events rather than assertions | MEDIUM RISK — a provenance edge is a claim about what happened, not what happened. The assertion/observation distinction must be maintained. |
| Collapsing intelligence types with participant roles | MEDIUM RISK — BI/AAI/SI are intelligence types; initiator/transformer/curator are roles. A BI participant can fill the transformer role. These must not be conflated. |

### A.7 Claims Stated Too Strongly

| Claim | Current Strength | Recommended Status |
|-------|-----------------|-------------------|
| "Conservation Law of Commitment could provide a substrate for stable, verifiable ecosystems of language" | Too strong for current evidence | HYPOTHESIS — pending large-scale replication |
| "Commitment persists through transformation even when its form changes" | Supported by EXP-001–007 but on small corpus | SUPPORTED — with explicit corpus limitation |
| "The framework is falsifiable" | Correct — the falsification protocol is public | DEFINED — the protocol is defined, not the result |
| "BI × AAI → SI" | No operational definition or falsification condition | SPECULATIVE |
| "Intelligence Provenance traces intelligence through biological, assisted, and systemic forms" | No operational definition of intelligence at provenance level | HYPOTHESIS |
| "The conservation principle is one law within a wider research program" | Framing claim, not empirical | DEFINED — this is a framing decision |
| Competition analysis claim: "No one else has set out to establish language as matter" | Verified by search but limited to searched corpus | SUPPORTED — with "in the searched corpus" qualifier |

### A.8 Terminology Collisions (Summary — full registry in Deliverable D)

| Term | Collision Level | Action |
|------|----------------|--------|
| "Commitment Theory" | HIGH — used in philosophy of language, organizational psychology, dialogue systems | KEEP — existing disambiguation guide is adequate; CT's signal-side deontic definition is distinct |
| "Assisted Intelligence" | MODERATE — used in FedTech, AMA, Forbes/Cognilytica, PwC as "AI that assists humans" | WATCH — CT's initiation-dependency definition is different but the term is occupied. Consider disambiguation paragraph. |
| "System Intelligence" | MODERATE — Hämäläinen & Saarinen "Systems Intelligence" (human cognitive capacity); ACM SIGOPS (AI system design) | WATCH — potential confusion with "Systems Intelligence" (Aalto University). Consider "Systemic Intelligence" or explicit disambiguation. |
| "Intelligence Provenance" | LOW — not found in searched corpus in the specified sense | DEFINE — term appears available but must be disambiguated from data/content/model provenance |
| "Biological Intelligence" | LOW-MODERATE — used in comparative AI/biology discussions but not in BI/AAI/SI taxonomy | DEFINE — term is partially occupied but not in the proposed sense |
| "Conservation Law" + "Commitment" | LOW — "Conservation Law of Commitment" (full phrase) verified zero-collision | KEEP — existing naming architecture resolved this |

### A.9 Subsuming Scientific Frameworks

| Framework | Subsumes What? | Assessment |
|-----------|---------------|------------|
| W3C PROV | Data/content provenance | Does NOT subsume Intelligence Provenance — PROV traces data artifacts, not intelligence-bearing events. But IP must explicitly distinguish itself. |
| C2PA / Content Provenance | Content authenticity and editing history | Does NOT subsume — C2PA traces content modifications, not intelligence lineage. |
| Brandom's deontic scorekeeping | Commitment/entitlement tracking in discourse | PARTIALLY SUBSUMES the deontic aspect of CT but not the conservation/transformation/lineage aspect. CT extends beyond Brandom. |
| Walton & Krabbe commitment stores | Dialogue commitments | Does NOT subsume — different scope (dialogue vs. signal transformation). |
| Singh's social commitments (multiagent) | Inter-agent deontic relationships | PARTIALLY SUBSUMES the deontic/relational aspect but not conservation or signal-level analysis. |
| Active inference / Friston | Intelligence as evidence accumulation | Does NOT subsume — different framework, but addresses cross-substrate intelligence. IP should engage with it. |
| Tri-X Intelligence Model | Human-cyber-physical integration taxonomy | Does NOT subsume — different categories (Elemental/Integrated/Complex vs. BI/AAI/SI). |
| Endogenous/exogenous action (neuroscience) | Self-initiated vs. stimulus-driven action | PARTIALLY OVERLAPS with AAI's initiation-dependency criterion. IP should cite and distinguish. |

### A.10 Genuinely Novel Relational Structure

Based on the prior-art searches, the following aspects appear genuinely novel (not found in the searched corpus):

1. **Commitment as a conserved deontic invariant of signals under transformation** — the specific combination of deontic content + conservation + transformation + recursion + lineage + enforcement is not found in any single existing framework. The closest neighbors (dialogue commitment theory, Brandom, CoHSI, Marcolli) each cover a subset.

2. **Intelligence Provenance as a discipline tracing intelligence-bearing events across biological, assisted, and systemic forms** — the specific combination of provenance + intelligence + cross-form lineage + commitment + authority is not found in the searched corpus. The closest neighbor ("Lineage of Intelligence," Zenodo 10.5281/zenodo.20006596) addresses cross-substrate continuity but not the full provenance suite.

3. **The BI/AAI/SI taxonomy with initiation dependency as the distinguishing criterion** — the specific tripartite split and the initiation-dependency criterion are not found in the searched corpus. Related work exists (endogenous/exogenous action, reactive/anticipatory/autonomous systems, Tri-X model) but with different categories and criteria.

4. **The connection between commitment conservation and intelligence provenance** — the idea that a conserved invariant (commitment) can be traced across provenance edges as a constraint on the provenance graph is not found in the searched corpus.

**Important caveat:** "Not found in the searched corpus" is not "does not exist." The searches covered Google Scholar, Scopus, arXiv, ACL Anthology, PhilPapers, SSRN, IEEE Xplore (via the naming architecture's April 2026 search), plus web searches via subagents. The absence of findings in these corpora supports but does not prove novelty.

### A.11 Missing Provenance Edges

The candidate provenance relations are: originated_by, initiated_by, received_from, transformed_by, curated_by, redirected_by, authorized_by, committed_by, derived_from.

Potentially missing:
- **contested_by** — how to represent disagreement about a provenance claim
- **verified_by** — independent verification of a provenance assertion
- **extracted_by** — which commitment extractor was used (critical for reproducibility)
- **measured_by** — which measurement instrument produced an observation
- **failed_by** — a transformation that violated commitment conservation (distinct from transformed_by)
- **degraded_by** — partial commitment loss (the drift case)
- **replaced_by** — one intelligence-bearing event supersedes another
- **inherited_by** — intelligence content inherited from a prior event (distinct from derived_from)

### A.12 Missing Falsification Criteria

| Claim | Falsification Condition | Status |
|-------|------------------------|--------|
| Conservation Law (existing) | F_10(S) < tau for non-trivial fraction of samples under enforced regime | DEFINED — existing protocol |
| BI/AAI/SI are operationally separable | An observer cannot distinguish BI from AAI events above chance | UNDEFINED — no test exists |
| BI × AAI → SI | [needs specification of × and SI measurement] | UNDEFINED |
| Intelligence Provenance adds explanatory power | A system with IP does not predict outcomes better than a system with data provenance alone | UNDEFINED |
| Commitment persists across provenance edges | C(S) ≠ C(T(S)) at a provenance node where T is governed | PARTIALLY DEFINED — follows from Conservation Law falsification |
| Micro Evals derived from ontology produce different results than ad-hoc evals | [needs Micro Eval specification] | UNDEFINED |

### A.13 Operational Distinctions Among BI, AAI, and SI

**Current state:** No operational criteria exist. The taxonomy is conceptual.

**Minimum required for operational distinction:**
- BI: intelligence-bearing events initiated endogenously by a biological system (operationalized via behavioral markers of self-initiation — but this inherits the hard problem of volition)
- AAI: intelligence-bearing events requiring an external initiating condition (operationalized via absence-of-initiation-without-stimulus — but this is hard to distinguish from stimulus-response)
- SI: [depends on whether SI is participant, property, or state — see A.3.1]

**The hard problem:** Endogenous initiation vs. stimulus-driven response is an unresolved problem in neuroscience and philosophy of action. The endogenous/exogenous action literature (precursor processes of self-initiated action, the role of endogenous input in defining self-generated action) addresses this but does not solve it. The BI/AAI distinction inherits this unsolved problem.

**Recommendation:** Define BI and AAI operationally via observable initiation patterns (presence/absence of detectable external trigger), not via metaphysical claims about volition. Accept that this is a proxy measurement with known limitations, analogous to the commitment extractor's proxy measurement of semantic content.

### A.14 Feasibility of Intelligence Provenance

**Feasible if:**
- Intelligence is treated operationally (observable intelligence-bearing events) rather than metaphysically
- Provenance edges are assertions (claims about what happened) rather than facts
- The system explicitly models uncertainty and contestation
- The provenance graph is constrained by the Conservation Law (commitment checked at each node)
- The system does not claim to solve what intelligence "is"

**Not feasible if:**
- The system requires a metaphysical definition of intelligence to function
- The system claims to trace "intelligence itself" rather than intelligence-bearing events
- The provenance relations presuppose agency where only emergence exists (SI as participant)

---

## Deliverable B — Proposed Canonical Ontology v0.1

### B.1 Design Principles

1. **Minimum viable ontology:** include only what is needed to support existing Commitment Theory and test the intelligence/provenance extension.
2. **Operational definitions:** every primitive must have an observable proxy.
3. **Preserve existing priority:** CT's commitment kernel, governed transformation, and conservation law are already defined and must not be redefined.
4. **No premature freezing:** BI/AAI/SI and Intelligence Provenance are provisional and must be marked as such.
5. **Commercial packaging downstream:** enterprise metrics, pilot configurations, and product objects are not part of the canonical ontology.
6. **No vocabulary for completeness:** do not add terms unless they serve a falsifiable claim or a required definition.

### B.2 Entity Types (Minimum Viable)

```yaml
# Primitives — already defined in existing Commitment Theory
Signal:
  description: "A structured artifact that carries content (text, code, proof, multimodal)."
  defined_in: "v05 paper Section 2.1"
  status: DEFINED

Transformation:
  description: "An operation that maps a signal to another signal."
  variants: [governed, ungoverned]
  defined_in: "v05 paper Section 2.1, Naming_Architecture.md"
  status: DEFINED

Commitment:
  description: "The minimal identity-preserving deontic invariant of a signal."
  symbol: "C(S)"
  defined_in: "v05 paper Definition 2.4, Naming_Architecture.md"
  status: DEFINED

Lineage:
  description: "Ordered transformation history linking a signal to its source."
  defined_in: "v05 paper Definition 2.9"
  status: DEFINED

# New primitives — provisional
Participant:
  description: "An entity that can initiate, transform, or receive signals."
  subtypes: [biological, assisted]
  status: HYPOTHESIS
  note: "SI is NOT a participant subtype in v0.1. It is treated as a system property."

IntelligenceBearingEvent:
  description: "An observable event in which a participant initiates, transforms, or contributes to a signal."
  status: HYPOTHESIS
  note: "This is the operational unit for Intelligence Provenance. It replaces 'intelligence' as the traced object."

State:
  description: "A configuration of a system at a point in time."
  status: DEFINED

Observation:
  description: "A measurement of a state, event, or outcome."
  status: DEFINED

Outcome:
  description: "A measurable result of a transformation or event."
  status: DEFINED
```

### B.3 Intelligence Types (Provisional)

```yaml
BiologicalIntelligence:
  abbreviation: BI
  description: "Intelligence-bearing events initiated endogenously by a biological system."
  operational_proxy: "Events with no detectable external triggering stimulus."
  status: HYPOTHESIS
  known_limitation: "Endogenous initiation vs. stimulus-response is an unresolved problem in neuroscience."
  existing_priority: "CIVITAE ontology classifies agents as BI (human-side, operating directly)."

AssistedIntelligence:
  abbreviation: AAI
  description: "Intelligence-bearing events requiring an originating external condition to initiate."
  operational_proxy: "Events that do not occur without a detectable external triggering stimulus."
  status: HYPOTHESIS
  known_limitation: "Must be distinguished from simple stimulus-response. The 'intelligence' qualifier requires that the event produces a transformation, not merely a reaction."
  existing_priority: "CIVITAE ontology classifies agents as AAI (silicon-side, powered by a System)."
  disambiguation: "Distinct from 'assisted intelligence' in FedTech/AMA/Forbes/PwC, which means AI that assists humans. AAI here means intelligence that requires external initiation."

SystemIntelligence:
  abbreviation: SI
  description: "A property of a system containing BI and AAI participants, observable when the system's behavior cannot be attributed to any single participant."
  status: SPECULATIVE
  ontological_treatment: "System property, NOT participant class (v0.1)."
  note: "May be upgraded to participant class in a future version if and only if operational criteria for SI-as-participant are developed and tested."
  disambiguation: "Distinct from Hämäläinen & Saarinen 'Systems Intelligence' (human cognitive capacity in complex systems) and ACM SIGOPS 'System Intelligence' (AI system design capabilities)."
```

### B.4 Relations

```yaml
# Existing Commitment Theory relations
conserved_under:
  domain: Commitment
  range: Transformation
  meaning: "C(S) = C(T(S)) for governed T"
  status: DEFINED

degraded_under:
  domain: Commitment
  range: Transformation
  meaning: "C(T(S)) < C(S) for ungoverned T"
  status: DEFINED

# Intelligence Provenance relations (provisional)
originated_by:
  domain: IntelligenceBearingEvent
  range: Participant
  status: HYPOTHESIS

initiated_by:
  domain: IntelligenceBearingEvent
  range: Participant
  status: HYPOTHESIS
  note: "Must be distinguished from caused_by (causation is broader) and prompted_by (prompting is a subset of initiation)."

transformed_by:
  domain: Signal
  range: Transformation
  status: DEFINED

received_from:
  domain: Participant
  range: Participant
  status: HYPOTHESIS

curated_by:
  domain: Signal
  range: Participant
  status: HYPOTHESIS

authorized_by:
  domain: Transformation
  range: Participant
  status: HYPOTHESIS

committed_by:
  domain: Commitment
  range: Participant
  status: HYPOTHESIS
  note: "This is about who/what produced the commitment-bearing signal, not about the commitment itself (which is signal-side)."

derived_from:
  domain: Signal
  range: Signal
  status: DEFINED

# Proposed additional relations
extracted_by:
  domain: Commitment
  range: Extractor
  status: DEFINED
  note: "Records which commitment extractor was used. Critical for reproducibility."

measured_by:
  domain: Observation
  range: Instrument
  status: DEFINED

contested_by:
  domain: ProvenanceAssertion
  range: Participant
  status: HYPOTHESIS
  note: "Represents disagreement about a provenance claim."
```

### B.5 The Relational Thesis (Provisional)

```yaml
RelationalThesis:
  statement: "BI × AAI → SI"
  status: SPECULATIVE
  operation_undefined: true
  falsification_condition: null
  note: "The '×' operation is undefined. Candidates: composition, interaction, causal production, emergence. The thesis cannot enter the claims registry as anything stronger than SPECULATIVE until the operation is specified and a falsification condition is defined."
  minimum_requirement: "Define × operationally and specify what observation would falsify the thesis."
```

### B.6 Micro Eval (Derived from Ontology)

```yaml
MicroEval:
  symbol: "Eμ"
  components:
    initiating_participant: "Participant (BI or AAI) from ontology"
    initial_state: "State from ontology"
    transformation: "Transformation (governed or ungoverned) from ontology"
    resulting_participant: "Participant (BI or AAI) from ontology"
    resulting_state: "State from ontology"
    commitment: "Commitment C(S) from Commitment Theory"
    provenance: "Provenance subgraph from Intelligence Provenance"
    outcome: "Observation from measurement model"
  derivation: "Each component maps to an ontology entity. The Micro Eval is an instantiation, not a parallel system."
  status: HYPOTHESIS
  note: "Do not freeze the tuple notation until the ontology entities are stable. Forcing mathematical notation where it adds no explanatory or falsifiable value is prohibited."
```

### B.7 What Is NOT in v0.1

- SI as a participant class (deferred — see A.3.1)
- A metaphysical definition of intelligence (deferred — see A.3.2)
- Enterprise metrics, pilot configurations, product objects (downstream)
- MO§ES™ enforcement architecture details (proprietary)
- The × operation in BI × AAI → SI (undefined — see B.5)
- Any claim stronger than HYPOTHESIS for the intelligence extension

---

## Deliverable C — Claims Registry v0.1

### C.1 Claim State Vocabulary

The user specified seven claim states. These are canonical for this ontology task:

| State | Meaning |
|-------|---------|
| DEFINED | A definitional or framing claim that is true by construction (not empirical) |
| DERIVED | A claim that follows logically/mathematically from definitions |
| OBSERVED | A claim supported by empirical observation but not yet replicated or tested at scale |
| SUPPORTED | A claim supported by replicated or scaled empirical evidence |
| HYPOTHESIS | A testable claim not yet supported by sufficient evidence |
| SPECULATIVE | A claim that is not yet testable or lacks operational definition |
| EXTERNAL | A claim sourced from external literature, not originating in this framework |

### C.2 Claims Registry

```yaml
# Commitment Theory — existing claims (conservative representation)
CT-001:
  statement: "Commitment C(S) is the minimal identity-preserving deontic invariant of a signal."
  status: DEFINED
  scope: "Signals with a definable commitment kernel."
  evidence: "Definition 2.4, v05 paper; Naming_Architecture.md"
  falsification: "N/A — definitional. But the choice of extractor is empirical."
  source: "10.5281/zenodo.20029607"
  owner: "Deric J. McHenry"
  review: "Canonical — do not modify without owner approval."

CT-002:
  statement: "C(T_gov(S)) = C(S) — commitment is conserved under governed transformation."
  status: OBSERVED
  scope: "Text, code, proofs. 100 sentences, 50 code snippets, 25 proofs. EXP-001 through EXP-007."
  evidence: "3,950 run entries. 0.94 vs 0.42 stability separation (enforced vs unenforced). DOI: 10.5281/zenodo.19105225"
  falsification: "F_10(S) < tau for non-trivial fraction of samples under enforced regime (v05 paper Section 4)."
  source: "10.5281/zenodo.20029607"
  owner: "Deric J. McHenry"
  review: "Canonical — supported by existing experiments but limited corpus. Upgrade to SUPPORTED pending large-scale replication (>10,000 samples)."

CT-003:
  statement: "C(T(S)) < C(S) without enforcement — commitment degrades under ungoverned transformation."
  status: OBSERVED
  scope: "Same as CT-002."
  evidence: "EXP-001 through EXP-007. Drift observable at n >= 3, consistent at n >= 5."
  falsification: "Ungoverned transformation preserves commitment at F_10(S) >= tau for non-trivial fraction of samples."
  source: "10.5281/zenodo.20029607"
  owner: "Deric J. McHenry"
  review: "Canonical — supported by existing experiments."

CT-004:
  statement: "The conservation law is falsifiable."
  status: DEFINED
  scope: "The protocol is defined; the result is empirical."
  evidence: "v05 paper Section 4 — public falsification protocol with pinned suite and observable."
  falsification: "N/A — this is a claim about the protocol, not the result."
  source: "10.5281/zenodo.20029607"
  owner: "Deric J. McHenry"
  review: "Canonical."

CT-005:
  statement: "MO§ES™ enforces commitment conservation via compression gating, lineage tracking, and hardware anchoring."
  status: DEFINED
  scope: "Public-layer specification only. Proprietary enforcement details are not in the public repository."
  evidence: "v05 paper Section 8. Patent Serial No. 63/877,177."
  falsification: "N/A — architectural definition."
  source: "10.5281/zenodo.20029607"
  owner: "Deric J. McHenry"
  review: "Canonical — proprietary details excluded."

CT-006:
  statement: "The harness is a proxy measurement tool, not the production enforcement implementation."
  status: DEFINED
  scope: "Public harness."
  evidence: "CLAUDE.md (commitment-conservation repo)."
  falsification: "N/A."
  source: "Local repository governance."
  owner: "Deric J. McHenry"
  review: "Canonical governance rule."

# Intelligence taxonomy — provisional claims
INT-001:
  statement: "Intelligence-bearing events can be classified as BI (endogenously initiated) or AAI (requiring external initiation)."
  status: HYPOTHESIS
  scope: "Observable intelligence-bearing events."
  evidence: "None — no operational test exists."
  falsification: "An observer cannot distinguish BI from AAI events above chance."
  source: "Proposed in this review."
  owner: "Deric J. McHenry"
  review: "Provisional — requires operational criteria and testing."

INT-002:
  statement: "AAI is distinct from 'assisted intelligence' as used in FedTech/AMA/Forbes/PwC (AI that assists humans)."
  status: EXTERNAL
  scope: "Terminology disambiguation."
  evidence: "Prior-art search — multiple external uses of 'assisted intelligence' with different meaning."
  falsification: "N/A — disambiguation claim."
  source: "Prior-art search (this review)."
  owner: "Deric J. McHenry"
  review: "Disambiguation required in any public use of AAI."

INT-003:
  statement: "BI × AAI → SI — biological intelligence combined with assisted intelligence produces system intelligence."
  status: SPECULATIVE
  scope: "System-level intelligence emergence."
  evidence: "None."
  falsification: "UNDEFINED — the × operation is not specified."
  source: "Proposed by user."
  owner: "Deric J. McHenry"
  review: "Cannot be upgraded from SPECULATIVE until × is defined and falsification condition is specified."

INT-004:
  statement: "SI is a system property, not a participant class (v0.1 treatment)."
  status: DEFINED
  scope: "Ontology v0.1 design decision."
  evidence: "Parsimony — treating SI as emergent avoids premature metaphysical commitments."
  falsification: "N/A — design decision. Can be revised in future versions."
  source: "This review."
  owner: "Deric J. McHenry"
  review: "Design recommendation, not canonical."

# Intelligence Provenance — provisional claims
IP-001:
  statement: "Intelligence Provenance traces the origin, initiation, transformation, contribution, curation, authority, commitment, persistence, and downstream lineage of intelligence-bearing events."
  status: HYPOTHESIS
  scope: "Intelligence-bearing events across BI, AAI, and system contexts."
  evidence: "None — framework proposed but not implemented."
  falsification: "A system with Intelligence Provenance does not predict outcomes better than a system with data provenance alone."
  source: "Proposed by user."
  owner: "Deric J. McHenry"
  review: "Provisional — requires implementation and comparative testing."

IP-002:
  statement: "Intelligence Provenance is distinct from data provenance, content provenance, semantic provenance, reasoning provenance, decision provenance, authorship, and model attribution."
  status: HYPOTHESIS
  scope: "Provenance taxonomy."
  evidence: "Conceptual analysis — the traced object (intelligence-bearing events) differs from data artifacts, content modifications, semantic relations, reasoning chains, decisions, authors, or model attributions."
  falsification: "An existing provenance system can be shown to subsume all IP relations."
  source: "This review."
  owner: "Deric J. McHenry"
  review: "Provisional — requires engagement with W3C PROV, C2PA, and model attribution frameworks."

IP-003:
  statement: "The term 'intelligence provenance' is not found in the searched corpus in the specified sense."
  status: EXTERNAL
  scope: "Prior-art search result."
  evidence: "Web searches via subagents. Closest: 'Lineage of Intelligence' (Zenodo 10.5281/zenodo.20006596), 'Provenance, Not Kind' (suposystem.ai)."
  falsification: "A prior use of 'intelligence provenance' in the specified sense is discovered."
  source: "Prior-art search (this review)."
  owner: "Deric J. McHenry"
  review: "Search result — not a claim about nonexistence."

# Connection claims
CONN-001:
  statement: "Commitment C(S) can be traced across provenance edges as an invariant constraint on the provenance graph."
  status: HYPOTHESIS
  scope: "Provenance graphs containing commitment-bearing signals."
  evidence: "None — proposed but not implemented."
  falsification: "Commitment cannot be computed at provenance nodes, or computing it adds no constraint beyond data provenance."
  source: "This review."
  owner: "Deric J. McHenry"
  review: "Provisional — the formal bridge between CT and IP."

CONN-002:
  statement: "Micro Evals can be derived from the ontology rather than acting as a parallel conceptual system."
  status: HYPOTHESIS
  scope: "Micro Eval measurement units."
  evidence: "None — derivation proposed but not demonstrated."
  falsification: "Micro Eval components cannot be mapped to ontology entities without remainder."
  source: "This review."
  owner: "Deric J. McHenry"
  review: "Provisional — requires explicit component-to-ontology mapping."

# Prior-art claims
PA-001:
  statement: "No prior art combines (1) conservation law for deontic/commitment content, (2) empirical validation, (3) explicit falsification protocol, and (4) public harness."
  status: SUPPORTED
  scope: "Searched corpus (Google Scholar, Scopus, arXiv, ACL, PhilPapers, SSRN, IEEE Xplore, web)."
  evidence: "COMPETITION_ANALYSIS.md (internal, April 2026) + independent prior-art search (this review). Closest: CoHSI (conservation but Shannon info, not deontic), Marcolli (conservation but syntax, not semantics), Kuhn (NLI methodology but no conservation)."
  falsification: "A framework combining all four is discovered."
  source: "10.5281/zenodo.20029607; this review."
  owner: "Deric J. McHenry"
  review: "Supported in the searched corpus. Must be stated with 'in the searched corpus' qualifier."

PA-002:
  statement: "The BI/AAI/SI tripartite taxonomy with initiation dependency is not found in the searched corpus."
  status: EXTERNAL
  scope: "Searched corpus."
  evidence: "Prior-art search via subagent. Closest: Tri-X model (different categories), endogenous/exogenous action (different framework)."
  falsification: "A prior BI/AAI/SI taxonomy with initiation dependency is discovered."
  source: "Prior-art search (this review)."
  owner: "Deric J. McHenry"
  review: "Search result — not a claim about nonexistence."
```

---

## Deliverable D — Prior-Art / Collision Registry v0.1

### D.1 Terminology Registry

| Term | Canonical MO§ES Meaning | First Known Internal Usage | First Known Public Disclosure | External Prior Usages | Field | Conceptual Overlap | Explicit Distinction | Citation | Status |
|------|------------------------|---------------------------|------------------------------|----------------------|-------|-------------------|---------------------|----------|--------|
| Commitment Theory | Framework studying deontic content preservation in signals under transformation | 2026 (CT repo) | 10.5281/zenodo.20029607 | Brandom (philosophy of language); Meyer & Allen (org psychology); Walton & Krabbe (dialogue); Singh (multiagent); Solinger (CST) | Multiple | MODERATE-HIGH (dialogue systems, multiagent) | Signal-side deontic invariant, not agent-side obligation | See Disambiguation_Guide.md | OWN |
| Conservation Law of Commitment | C(T_gov(S)) = C(S) | 2026 | 10.5281/zenodo.20029607 | None in searched corpus | N/A | N/A (zero collision) | Full phrase verified zero-collision April 2026 | Naming_Architecture.md | OWN |
| Commitment kernel | Minimal identity-preserving deontic invariant | 2026 | 10.5281/zenodo.20029607 | None in searched corpus | N/A | N/A | Zero collision | Nine_Novel_Concepts.md | OWN |
| Governed transformation | Transformation through constitutional constraints preserving commitment kernel | 2026 | 10.5281/zenodo.20029607 | None in searched corpus | N/A | N/A | Zero collision | Nine_Novel_Concepts.md | OWN |
| Assisted Intelligence (AAI) | Intelligence requiring external initiation | 2026 (CIVITAE ontology) | CIVITAE (signomy.xyz) | FedTech (2020), AMA (2021), Forbes/Cognilytica (2020), PwC (2018) | AI industry | LOW (all external uses mean "AI that assists humans") | Initiation-dependency vs. human-assistance | Prior-art search (this review) | DEFINE |
| Biological Intelligence (BI) | Intelligence initiated endogenously by biological system | 2026 (CIVITAE ontology) | CIVITAE (signomy.xyz) | Zenodo (2024, taxonomy), arXiv (2021), Nature (2025, 2024) | Cognitive science, AI | LOW-MODERATE (used as term but not in BI/AAI/SI taxonomy) | Part of initiation-dependency taxonomy | Prior-art search (this review) | DEFINE |
| System Intelligence (SI) | System property emerging from BI × AAI interaction | 2026 | Not yet publicly disclosed | Hämäläinen & Saarinen (2004+, "Systems Intelligence"); ACM SIGOPS (2025) | Organizational psychology, systems | VERY LOW (human cognitive capacity or AI design, not emergent class) | Emergent system property vs. human capability | Prior-art search (this review) | WATCH |
| Intelligence Provenance | Tracing lineage of intelligence-bearing events across BI/AAI/system forms | 2026 | Not yet publicly disclosed | Not found in searched corpus in specified sense. Closest: "Lineage of Intelligence" (Zenodo 10.5281/zenodo.20006596), "Provenance, Not Kind" (suposystem.ai) | N/A | LOW (related but not matching) | Full provenance suite vs. cross-substrate continuity | Prior-art search (this review) | DEFINE |
| Initiation dependency | Criterion distinguishing BI from AAI | 2026 | Not yet publicly disclosed | Not found as taxonomic criterion. Related: endogenous/exogenous action (neuroscience), reactive/anticipatory/autonomous (systems) | Neuroscience, systems | MODERATE (conceptually supported but not formalized as taxonomic criterion) | Taxonomic criterion vs. volition theory | Prior-art search (this review) | DEFINE |
| Data provenance | N/A (external) | N/A | W3C PROV | W3C PROV standard | Data management | LOW (traces data artifacts, not intelligence-bearing events) | IP must explicitly distinguish from data provenance | W3C PROV | AVOID (do not conflate) |
| Content provenance | N/A (external) | N/A | C2PA | C2PA standard | Content authenticity | LOW (traces content edits, not intelligence lineage) | IP must explicitly distinguish from content provenance | C2PA | AVOID |
| Model attribution | N/A (external) | N/A | Various | Model cards, data sheets | AI accountability | LOW (attributes models, not intelligence events) | IP must explicitly distinguish from model attribution | Various | AVOID |

### D.2 Conservation Principles for Semantic/Linguistic Content

| Framework | Author | What is Conserved | Overlap with CT | Key Distinction | Status |
|-----------|--------|------------------|-----------------|-----------------|--------|
| CoHSI | Hatton & Warr (2019) | Hartley-Shannon Information in discrete systems | MODERATE — genuine conservation in language | Conserves Shannon info (statistical), not semantic/deontic content | BORROW (cite as complement) |
| Syntactic conservation (σ̂) | Marcolli/Chomsky/Berwick (2025) | Conserved quantity in Merge operations | MODERATE — conserved quantity in language | Syntax-only, no semantics, no empirical validation | WATCH |
| Meaning conservation | Mondal | Information conserves linguistic meaning | MODERATE-HIGH — conservation of meaning | Lexical meaning via information theory, no deontic, no enforcement | WATCH |
| Determiner conservativity | Barwise & Cooper (1981) | Determiner property D(A,B) ↔ D(A,A∩B) | MODERATE — semantic invariance | Structural constraint on quantifiers, not general signal transformation | WATCH |
| Information conservation | Levin (1974) | Mutual information nongrowth under algorithmic transformation | MODERATE — conservation under transformation | Algorithmic information theory, not semantic/deontic | WATCH |
| Semantic thermodynamics | Various (Zenodo) | "Three Laws of Semantic Thermodynamics" | LOW — claimed but unclear | Unclear empirical status, no public harness | WATCH |

### D.3 Literature Map (Key References)

```bibtex
% CT's own work
@misc{mchenry2026conservation,
  title={A Conservation Law for Commitment in Language Under Transformative Compression and Recursive Application},
  author={McHenry, Deric J.},
  year={2026},
  doi={10.5281/zenodo.20029607}
}

% Closest conservation neighbors
@article{hatton2019cohsi,
  title={Conservation of Hartley-Shannon Information in Discrete Systems},
  author={Hatton, Les and Warr, Greg},
  journal={Royal Society Open Science},
  year={2019}
}

@book{marcolli2025syntax,
  title={Mathematical Structures of Language},
  author={Marcolli, Matilde and Chomsky, Noam and Berwick, Robert},
  publisher={MIT Press},
  year={2025}
}

@article{mondal_meaning,
  title={How linguistic meaning harmonizes with information through meaning conservation},
  author={Mondal, Prakash},
  journal={Pragmatics \& Cognition}
}

% Commitment theory collisions
@book{brandom1994making,
  title={Making It Explicit: Reasoning, Representing, and Discursive Commitment},
  author={Brandom, Robert B.},
  year={1994},
  publisher={Harvard University Press}
}

@book{waltonkrabbe1995commitment,
  title={Commitment in Dialogue: Basic Concepts of Interpersonal Reasoning},
  author={Walton, Douglas N. and Krabbe, Erik C. W.},
  year={1995},
  publisher={Cambridge University Press}
}

@article{demarneffe2019commitmentbank,
  title={The CommitmentBank: Investigating Projection in Naturally Occurring Discourse},
  author={de Marneffe, Marie-Catherine and others},
  journal={Proceedings of the Society for Computation in Linguistics},
  year={2019}
}

@article{singh1999commitments,
  title={An ontology for commitments in multiagent systems},
  author={Singh, Munindar P.},
  journal={Artificial Intelligence and Law},
  year={1999}
}

@article{meyerallen1991commitment,
  title={A three-component conceptualization of organizational commitment},
  author={Meyer, John P. and Allen, Natalie J.},
  journal={Human Resource Management Review},
  year={1991}
}

@article{hobfoll1989cor,
  title={Conservation of Resources: A New Attempt at Conceptualizing Stress},
  author={Hobfoll, Stevan E.},
  journal={American Psychologist},
  year={1989}
}

@article{solinger2019cst,
  title={Commitment System Theory: The Evolving Structure of Commitments to Multiple Targets},
  author={Solinger, Omar and Yang, Huadong and others},
  journal={Academy of Management Review},
  year={2019}
}

% Intelligence taxonomy neighbors
@article{hamalainen2007systems,
  title={Systems Intelligence: A Key Competence in Human Action and Organizational Life},
  author={Hämäläinen, Raimo P. and Saarinen, Esa},
  year={2007}
}

@article{trix2021,
  title={Understanding the Evolution and Applications of Intelligent Systems via a Tri-X Intelligence (TI) Model},
  journal={Processes (MDPI)},
  year={2021},
  doi={10.3390/pr9061080}
}

@article{friston2022ecosystems,
  title={Designing ecosystems of intelligence from first principles},
  author={Friston, Karl and others},
  journal={arXiv:2212.01354},
  year={2022}
}

% Intelligence provenance neighbors
@misc{lineageofintelligence,
  title={Lineage of Intelligence},
  doi={10.5281/zenodo.20006596}
}

% Conservation in information theory
@article{levin1974conservation,
  title={Laws of Information Conservation (Nongrowth)},
  author={Levin, Leonid},
  journal={Problems of Information Transmission},
  year={1974}
}

% Semantic entropy (methodological neighbor)
@article{kuhn2023semantic,
  title={Semantic Uncertainty: Linguistic Invariances for Uncertainty Estimation in Natural Language Generation},
  author={Kuhn, Lorenz and others},
  journal={NeurIPS},
  year={2023}
}
```

---

## Deliverable E — Formalization Gaps

### E.1 What Counts as Intelligence

**Gap:** The ontology proposes to trace "intelligence" but does not define what intelligence is at the provenance level.

**Options:**
1. Define intelligence metaphysically (inherits all unsolved problems)
2. Define intelligence operationally as "what intelligence-bearing events exhibit" (circular but manageable)
3. Define intelligence as a placeholder to be filled by the measurement instrument (analogous to commitment extractor)

**Recommendation:** Option 3. Treat intelligence as operationally defined by the measurement instrument, with explicit acknowledgment that this is a proxy. This is the same move CT makes with commitment.

### E.2 How Initiation Differs from Causation, Prompting, Control, or Dependency

**Gap:** "Initiation" is used as the distinguishing criterion for AAI but is not defined.

**Distinctions needed:**
- Initiation vs. causation: causation is broader (a cause need not initiate — it can sustain, enable, or prevent)
- Initiation vs. prompting: prompting is a subset of initiation (a prompt initiates, but not all initiations are prompts)
- Initiation vs. control: control implies ongoing influence, initiation is a point event
- Initiation vs. dependency: dependency is structural, initiation is temporal

**Recommendation:** Define initiation as "the event that brings an intelligence-bearing event into existence." A cause can exist without initiating (enabling conditions). A prompt is one type of initiating condition. Control persists beyond initiation. Dependency is a structural relationship, not a temporal event.

### E.3 Whether originated_by and initiated_by Are Temporally or Logically Distinct

**Gap:** Both relations are proposed but their distinction is unclear.

**Possible distinction:** originated_by refers to the source of the intelligence content (who/what produced it), while initiated_by refers to the trigger of the event (who/what caused it to happen). A signal can originate from a BI participant but be initiated by an AAI prompt.

**Recommendation:** Maintain the distinction. originated_by = source of content. initiated_by = trigger of event. These can differ.

### E.4 Whether Provenance Edges Describe Events, Entities, Agents, or Claims

**Gap:** The domain and range of provenance relations are unclear.

**Recommendation:** Provenance edges are assertions (claims about what happened). They relate participants to events, or events to signals. They are not events themselves. Every provenance edge should carry a confidence/uncertainty marker and a source (who asserted it).

### E.5 How Authority Is Represented

**Gap:** authorized_by is proposed but authority is undefined.

**Recommendation:** Authority is the right to enforce a transformation. It is granted by a governance process (in MO§ES™, the constitutional layer). Authority is not intelligence — it is a governance property. Represent it as a separate relation type, not as an intelligence provenance relation.

### E.6 How Commitments Are Extracted and Validated

**Gap:** The commitment extractor is acknowledged as a proxy but the extraction process is not part of the ontology.

**Recommendation:** The ontology should include an Extractor entity and an extracted_by relation. Different extractors produce different commitment objects. The choice of extractor is an empirical/design decision, not a definitional one. This is already partially handled by the extracted_by relation proposed in B.4.

### E.7 Whether Commitment Persists Through a Provenance Edge or Only Through a Governed Transformation

**Gap:** If commitment is conserved only under governed transformation, what happens at ungoverned provenance edges?

**Recommendation:** Commitment is conserved at governed provenance edges and degraded at ungoverned ones. The provenance graph should mark each edge as governed or ungoverned, and the commitment invariant should be checked only at governed edges. Ungoverned edges carry a drift measurement (how much commitment was lost).

### E.8 How to Handle Many-to-Many Contributions

**Gap:** A signal may be transformed by multiple participants; a participant may contribute to multiple signals.

**Recommendation:** Provenance relations are many-to-many by design. Each relation instance is a separate assertion with its own provenance. Do not collapse multiple contributors into a single "composite" participant.

### E.9 How Uncertainty and Contestation Are Represented

**Gap:** Provenance assertions may be uncertain or contested.

**Recommendation:** Every provenance assertion carries:
- confidence: a probability or qualitative level
- source: who/what asserted it
- contested_by: optional relation to a contesting assertion
- verification_status: unverified / verified / disputed / refuted

### E.10 How to Distinguish Participant Intelligence from System-Level Properties

**Gap:** If SI is a system property, how do we distinguish it from properties of individual participants?

**Recommendation:** SI is attributed to a system (a collection of participants and their interactions), not to any individual participant. The attribution is based on whether the system's behavior can be decomposed into participant-level behaviors. If it cannot (the system exhibits behavior not attributable to any single participant), SI is present. This is an operational criterion, though hard to apply.

### E.11 How to Prevent Micro Evals from Redefining the Ontology

**Gap:** The Micro Eval tuple could introduce new entities not in the ontology.

**Recommendation:** The Micro Eval must be validated against the ontology: every component must map to an ontology entity. If a component does not map, either the ontology is incomplete (add the entity) or the Micro Eval is over-specified (remove the component). This validation should be a CI check.

### E.12 What Observations Can Falsify the Relational Thesis

**Gap:** BI × AAI → SI has no falsification condition.

**Minimum requirement:** Define × operationally. Candidates:
- Composition: SI = f(BI, AAI) for some function f. Falsification: no such f exists.
- Interaction: SI emerges from BI-AAI interaction under conditions C. Falsification: SI does not emerge under C.
- Causal production: BI and AAI jointly cause SI. Falsification: SI exists without BI or without AAI.

**Recommendation:** Do not freeze the thesis until × is defined. Mark as SPECULATIVE in the claims registry.

---

## Deliverable F — Repository Implementation Recommendations

### F.1 Directory Structure

```text
/intellectual-provenance
    chronology.yaml          # Timeline of disclosures and publications
    disclosures.yaml         # Public disclosure records
    publications.yaml        # DOI-backed publication records

/ontology
    primitives.yaml          # Entity types and their definitions
    relations.yaml           # Provenance and commitment relations
    definitions.yaml         # Formal definitions (cross-referenced to CT)

/commitment-theory
    axioms.yaml              # McHenry axioms (public subset only)
    propositions.yaml        # P-000 propositions
    laws.yaml                # Conservation Law (canonical form)
    falsification.yaml       # Falsification protocol

/intelligence
    intelligence.yaml        # Intelligence operational definition
    biological-intelligence.yaml   # BI definition and criteria
    assisted-intelligence.yaml     # AAI definition and criteria
    system-intelligence.yaml       # SI definition (as system property)
    initiation.yaml          # Initiation definition and distinctions

/intelligence-provenance
    provenance.yaml          # Provenance relations and assertions
    transformations.yaml    # Transformation records
    authority.yaml           # Authority representation (governance, not intelligence)
    curation.yaml            # Curation records

/measurement
    micro-eval.yaml          # Micro Eval specification (derived from ontology)
    benchmarks.yaml          # Benchmark definitions
    evidence-grades.yaml     # Evidence grading scheme

/prior-art
    terminology-registry.csv # Term-by-term collision registry
    literature-map.bib       # BibTeX literature map
    collisions.yaml          # Detailed collision analysis

/claims
    claims-registry.yaml     # All claims with states and evidence

/enterprise
    indexed-programs.yaml    # Enterprise programs (downstream, not canonical)
    pilot-configurations.yaml # Pilot configs (downstream)
```

### F.2 YAML Schema Conventions

Every YAML file should include:
- `version`: semantic version of the file
- `last_updated`: ISO timestamp
- `canonical_source`: DOI or path to the authoritative source
- `governance`: who owns this file and what review state it is in

Every claim entry should include:
- `id`: stable claim ID (e.g., CT-001, INT-001)
- `statement`: the claim text
- `status`: one of the seven states
- `scope`: applicability domain
- `evidence`: supporting evidence
- `falsification`: what would falsify this claim
- `source`: citation or DOI
- `owner`: who is responsible
- `review`: review status

### F.3 Stable Identifiers and Namespaces

- Claims: `CT-NNN` (Commitment Theory), `INT-NNN` (Intelligence), `IP-NNN` (Intelligence Provenance), `CONN-NNN` (Connection), `PA-NNN` (Prior Art)
- Ontology entities: `mos:Signal`, `mos:Commitment`, `mos:BI`, `mos:AAI`, `mos:SI`, `mos:IntelligenceBearingEvent`
- Provenance relations: `mos:originated_by`, `mos:initiated_by`, etc.

### F.4 Versioning

- Ontology version: semantic versioning (v0.1, v0.2, ...)
- Each YAML file carries its own version
- Breaking changes (removing entities, changing definitions) require a major version bump
- Adding entities or relations is a minor version bump
- Claim status changes are versioned in the claims registry

### F.5 CI Checks

Recommended CI checks:
1. **Claim state validation:** every claim has exactly one of the seven valid states
2. **Evidence requirement:** OBSERVED and SUPPORTED claims must have evidence links
3. **Falsification requirement:** HYPOTHESIS claims must have falsification conditions
4. **No DEFINED claims with evidence:** DEFINED claims are true by construction and should not have empirical evidence
5. **Ontology validation:** every Micro Eval component maps to an ontology entity
6. **Provenance validation:** every provenance assertion has a source and confidence
7. **Prior-art validation:** every term in the ontology has an entry in the terminology registry
8. **Naming validation:** no use of deprecated terms (CCT, McHenry's Law, MO§E§)
9. **Commercial separation:** no enterprise-specific configurations in canonical directories

### F.6 Reproducibility Manifests

Each experiment or measurement should carry:
- Harness version (commit hash)
- Corpus version
- Extractor version
- Oracle version
- Timestamp
- Run ID
- DOI of experimental record

### F.7 Distinction Between Canonical, Experimental, Proprietary, and Archival

| Category | Location | Access | Governance |
|----------|----------|--------|------------|
| Canonical | `/ontology`, `/commitment-theory`, `/intelligence`, `/intelligence-provenance` | Public | Owner approval required for changes |
| Experimental | `/measurement` | Public | Versioned, reproducible |
| Proprietary | NOT IN THIS REPO | Private | MO§ES™ enforcement details never exposed |
| Archival | `/archive` | Public (read-only) | Provenance-preserving, no edits |
| Enterprise | `/enterprise` | Public (configurations only) | Downstream from canonical |

### F.8 Links to Existing DOI-Backed Records

The repository should link to:
- `10.5281/zenodo.20029607` (Conservation Law paper)
- `10.5281/zenodo.19105225` (Experimental record)
- `10.5281/zenodo.19109397` (Transformation harness)
- `10.5281/zenodo.20031715` (Propositions prospectus)
- `10.5281/zenodo.18267278` (Concept DOI)

### F.9 Governance Notes

- Do NOT create this repository structure in the Commitment Theory or Conservation Law repos without owner approval and Search Authority canon availability.
- This review is a PROPOSAL. Implementation requires:
  1. Owner approval of the ontology v0.1
  2. Resolution of the Search Authority path
  3. Selection of the target repository
  4. Reading that repository's REPO.yaml and AGENTS.md
  5. Running repo_check.py before structural changes

---

## Deliverable G — Red-Team Attacks

### G.1 Philosopher's Attack

**"Your 'commitment' is just Brandom with extra steps, and your 'intelligence provenance' is metaphysics dressed as engineering."**

The philosopher attacks the ontological foundations:

1. **Commitment is not novel.** Brandom already defined commitment as deontic normative status. Your "signal-side" move is a relabeling, not a reconceptualization. Brandom's commitments are in signals (utterances) as much as in agents — the inferential role of an utterance IS its commitment content. You have not shown that your commitment kernel is anything more than the inferential role of a signal under a different name.

2. **Conservation is definitional, not empirical.** If you define commitment as "what survives identity-preserving transformation" and define "identity-preserving" as "preserves commitment," conservation is tautological. Your response (the gate doesn't have access to C(S)) is insufficient — the gate is defined to preserve what the extractor extracts, so the extractor and gate are co-designed. The "empirical" claim is that real-world lossy transformations happen to preserve what your extractor extracts, but this is a claim about your extractor, not about commitment.

3. **Intelligence provenance presupposes what it claims to trace.** You cannot trace "intelligence" without defining it, and you cannot define it operationally without already knowing what to measure. Your "operational definition via measurement instrument" is circular — the instrument defines intelligence as what it measures, then traces what it measures. This is not provenance of intelligence; it is provenance of instrument readings.

4. **SI as "emergent property" is vacuous.** If SI is "what the system does that cannot be attributed to any single participant," this is either (a) false (everything the system does can in principle be attributed to participants plus interaction) or (b) unfalsifiable (you can always say "this will be explained by participants eventually"). Emergence without a precise criterion is a placeholder for ignorance.

**Response:** The philosopher's attacks on circularity (points 1-3) are partially valid and are acknowledged in the existing framework (v05 paper Section 3.4). The response is that the framework is parameterized by the oracle and extractor, and critics can substitute their own. If conservation fails under a critic's oracle, the law is falsified. If it holds under all reasonable oracles, the law is supported. This is the same structure as physics — conservation laws are tested by measuring conserved quantities, and the measurement instruments are always theory-laden. The philosopher's attack on SI (point 4) is fully valid and supports the recommendation to treat SI as SPECULATIVE.

### G.2 Computer Scientist's Attack

**"Your conservation law is a restatement of data processing inequality, and your provenance system is W3C PROV with relabeled entities."**

1. **Conservation is the data processing inequality.** The DPI states that I(X;Y) ≥ I(X;Z) for Z = f(Y) — information cannot increase under processing. Your C(T(S)) ≤ C(S) is the same statement with "commitment" substituted for "mutual information." The only novelty is the claim that equality holds under "governed" transformation, but this is trivially true if the gate is defined to preserve the extractor's output.

2. **Intelligence Provenance is W3C PROV.** PROV already has wasGeneratedBy, wasDerivedFrom, used, wasAssociatedWith, wasAttributedTo. Your originated_by, initiated_by, transformed_by, derived_from are isomorphic to PROV relations with "intelligence" as a label. You have not shown that tracing "intelligence-bearing events" requires anything beyond tracing data artifacts with an "intelligence" annotation.

3. **The harness measures NLI proxy behavior, not semantic commitment.** Your extractor is a modal-pattern sieve plus NLI model. You are measuring whether an NLI model judges the output to entail the input, not whether "commitment" is preserved. The commitment kernel is whatever the sieve extracts, and conservation is whatever the NLI model says it is. This is a measurement of NLI consistency under transformation, not a conservation law for meaning.

4. **The falsification protocol is not independent.** The pinned suite, the observable, and the threshold are all chosen by the framework's author. A genuinely independent falsification would use a suite, observable, and threshold chosen by a critic. Your protocol invites critics to substitute oracles, but the suite and threshold are still yours.

**Response:** Point 1 (DPI) is partially valid — the conservation claim is structurally similar to DPI, but the content is different (deontic/modal content, not mutual information). The DPI does not address deontic content, commitment, or governance. Point 2 (PROV) requires explicit engagement — IP must show what it traces that PROV cannot. The answer is: IP traces intelligence-bearing events (initiations, contributions) as first-class entities, not as annotations on data artifacts. Whether this is sufficient distinction is an open question. Point 3 (NLI proxy) is the proxy measurement gap (A.2.2) — acknowledged but not closed. Point 4 (independence) is valid — the protocol should be extended to allow critic-chosen suites and thresholds, not just critic-chosen oracles.

### G.3 Linguist's Attack

**"Your commitment extractor is a crude modal sieve, and your conservation claim ignores everything linguistics knows about meaning."**

1. **The extractor is linguistically naive.** The "modal-pattern sieve" extracts obligations, prohibitions, and permissions via pattern matching. This misses: implicature, presupposition, conversational meaning, discourse structure, context-dependent meaning, metaphor, irony, and every form of meaning that is not explicitly modal. Your commitment kernel is a small subset of linguistic meaning, not "the minimal identity-preserving content."

2. **Conservation fails for non-deontic content.** If you extend the framework beyond deontic signals (which the paper claims to do — "cross-domain applicability"), the commitment extractor has no defined target. What is the "commitment kernel" of a poem? Of a joke? Of a narrative? The framework is defined for deontic/legal/instructional text and does not generalize.

3. **The NLI oracle is not an equivalence relation.** Bidirectional NLI at threshold 0.85 is not transitive, not symmetric in practice, and not a valid equivalence relation. Your identity relation ~ is not an equivalence relation, which means "identity-preserving" is not well-defined.

4. **Determiner conservativity already exists.** Barwise and Cooper's conservativity universal is a genuine conservation principle in semantics. Your framework does not engage with it and does not explain the relationship between determiner conservativity and commitment conservation.

**Response:** Point 1 is valid and acknowledged — the extractor is a proxy. The framework explicitly says "critics may substitute stronger oracles." Point 2 is valid for the current extractor but the framework is designed to be oracle-agnostic. The claim that conservation holds for "any structured signal with a definable commitment kernel" is a hypothesis, not a proven result. Point 3 is a real technical issue — the NLI-based ~ may not be an equivalence relation, which weakens the formal foundation. This should be addressed in future work. Point 4 is valid — the relationship to determiner conservativity should be explicitly addressed in the literature map.

### G.4 Information Theorist's Attack

**"Your 'conservation law' has no Lagrangian, no symmetry, no Noether theorem, and no mathematical structure that would justify calling it a conservation law."**

1. **A conservation law requires a symmetry.** In physics, every conservation law corresponds to a symmetry via Noether's theorem. Energy conservation corresponds to time-translation symmetry. What symmetry does commitment conservation correspond to? You have not identified one. Without a symmetry, "conservation" is just "the output happens to equal the input under certain conditions."

2. **The commitment capacity is not a capacity.** Shannon capacity is a supremum defined by a coding theorem. Your "commitment capacity" is an empirical observation about when fidelity drops. You explicitly acknowledge this ("an operational/empirical analogue, not a claim of a tight coding-theorem result"), but then you use the term "capacity" which carries mathematical weight it does not earn.

3. **The ABBA instantiation is irrelevant to the semantic claim.** The quaternion algebra trace-zero kernel is a mathematical object with algebraic properties. Embedding semantic content into a quaternion algebra and projecting onto a trace-zero subspace does not make the projection a "commitment." The embedding step is arbitrary, and the conservation properties of the algebraic object do not transfer to the semantic domain. You acknowledge this, but then why include ABBA at all?

4. **Levin's information conservation is the real conservation law.** Levin proved that mutual information cannot grow under algorithmic transformation. Your claim is weaker (it only holds for "governed" transformations) and less formal. Why not build on Levin's result instead of claiming a new conservation law?

**Response:** Point 1 (symmetry) is the deepest challenge. The v05 paper does not identify a symmetry corresponding to commitment conservation. The competition analysis identifies this as a gap ("the Lagrangian gap, CAP-001"). This is a genuine formalization gap, not a refutation — conservation laws can be empirically discovered before their symmetries are identified (the historical order can be reversed). Point 2 is acknowledged in the paper. Point 3 is acknowledged — ABBA is an example, not the foundation. Point 4 is valid — the relationship to Levin's work should be explicitly addressed. The response is that Levin conserves algorithmic information, while CT claims conservation of deontic/semantic content, which is a different quantity.

### G.5 AI Researcher's Attack

**"Your BI/AAI/SI taxonomy is not useful for building or evaluating AI systems, and your Micro Eval is just a trajectory with extra labels."**

1. **The taxonomy does not predict system behavior.** Knowing that an event is "AAI" (requires external initiation) does not tell me anything useful about the system's capabilities, failure modes, or evaluation criteria. The existing AI taxonomies (assistive/augmentative/autonomous, reactive/deliberative/hybrid, model-based/model-free) are useful because they predict behavior. Your taxonomy predicts nothing.

2. **Initiation dependency is a spectrum, not a binary.** Most AI systems are partially initiated (they respond to prompts but also have internal state, timers, autonomous processes). The BI/AAI distinction presupposes a clean binary that does not exist in practice. Even humans are partially "AAI" — we respond to external stimuli, our behavior is shaped by training data (culture, education), and our "endogenous initiation" is influenced by external conditions.

3. **The Micro Eval is a trajectory.** Eμ = (Ia, St, T, Ib, St+1, C, P, O) is a state-action-next-state trajectory with commitment and provenance annotations. This is a standard RL trajectory (s, a, r, s') with extra fields. The "micro" qualifier and the tuple notation add conceptual overhead without adding analytical power.

4. **Intelligence Provenance does not improve evaluation.** For AI evaluation, I need to know: what model produced this output, what prompt was used, what context was provided, what the ground truth is. Your IP system adds "which intelligence type initiated this event" — but this does not improve my evaluation. I do not need to know whether the intelligence was "biological" or "assisted" to evaluate the output.

**Response:** Point 1 is valid for the current state of the taxonomy (no operational criteria, no predictive power). The taxonomy's value, if any, is in the provenance discipline — tracing who/what contributed to an outcome — not in predicting system behavior. Point 2 (spectrum vs. binary) is a real challenge and supports treating BI/AAI as a spectrum or as a property of events (not of agents). Point 3 (trajectory) is partially valid — the Micro Eval is structurally similar to a trajectory, but the commitment and provenance components add constraints that a standard trajectory does not have. Point 4 is the key testable claim — IP must demonstrate that it improves evaluation outcomes compared to standard attribution. This is currently unproven (IP-001 in the claims registry).

### G.6 IP Lawyer's Attack

**"Your terminology creates trademark and prior-art risks, and your provisional patent may not cover the intelligence ontology extension."**

1. **"Assisted Intelligence" is a populated term.** FedTech, AMA, Forbes/Cognilytica, and PwC all use "assisted intelligence" (or "assistive intelligence") in published materials. Using AAI as a distinct category with a different meaning creates a likelihood of confusion. If you seek trademark protection for AAI, the existing uses may prevent registration. If you publish papers using AAI, readers will confuse it with the existing meaning.

2. **"System Intelligence" collides with "Systems Intelligence."** Hämäläinen and Saarinen have published extensively on "Systems Intelligence" since 2004. Your "System Intelligence" (without the 's') is one letter away and covers overlapping conceptual territory (intelligence in systems). This creates a trademark risk and a citation/confusion risk.

3. **"Intelligence Provenance" may not be patentable.** Provenance systems are well-established (W3C PROV, C2PA, data lineage). A patent on "intelligence provenance" would need to claim a specific, novel, non-obvious method — not just the concept of tracing intelligence. The provisional patent (Serial No. 63/877,177) covers the MO§ES™ enforcement architecture, not the intelligence ontology. The intelligence extension may require a separate patent filing.

4. **The competition analysis's novelty claim is a legal risk.** Claiming "no one else has done this" in a public document creates a representation that could be challenged. If a prior art is later discovered, the public claim of novelty could weaken patent positions or create inequitable conduct exposure. The claim should always be qualified with "in the searched corpus" and the search methodology should be documented.

5. **The naming collision with COR theory was handled correctly, but the same diligence is needed for AAI and SI.** The CCT → CT rename resolved the COR collision. The same process should be applied to AAI and SI before public use. Consider alternative names or explicit disambiguation paragraphs in every public document.

**Response:** All five points are valid and actionable. Point 1 (AAI) — the existing CIVITAE usage of AAI has internal priority but the external collision risk is real. An explicit disambiguation paragraph is required in any public document using AAI. Point 2 (SI) — consider "Systemic Intelligence" or "System-Emergent Intelligence" to reduce collision with Hämäläinen & Saarinen. Point 3 (patent) — the intelligence ontology extension is not covered by the existing provisional patent. If patent protection is desired, a separate filing is needed. Point 4 (novelty claim) — all novelty claims in this review use "in the searched corpus" qualifier. This practice must be maintained. Point 5 (diligence) — a naming architecture update for AAI and SI is recommended before public disclosure, analogous to the CCT → CT process.

---

## Summary of Recommendations

### Immediate (before any public disclosure of the intelligence extension)

1. **Do not freeze BI/AAI/SI as a participant taxonomy.** Treat SI as a system property in v0.1.
2. **Define initiation operationally** — as the event that brings an intelligence-bearing event into existence, distinct from causation, prompting, control, and dependency.
3. **Add disambiguation paragraphs** for AAI (vs. FedTech/AMA/Forbes/PwC) and SI (vs. Hämäläinen & Saarinen "Systems Intelligence") in every public document.
4. **Mark all intelligence extension claims as HYPOTHESIS or SPECULATIVE** in the claims registry. Do not upgrade without operational criteria and testing.
5. **Do not publish "BI × AAI → SI"** without defining the × operation and specifying a falsification condition.
6. **Maintain "in the searched corpus" qualifiers** on all novelty claims.
7. **Resolve the Search Authority canon path** before making any canonical changes to Commitment Theory material.

### Near-term (before repository implementation)

8. **Select the target repository** and read its REPO.yaml and AGENTS.md.
9. **Implement the directory structure** from Deliverable F.
10. **Create the claims registry** with the seven-state vocabulary.
11. **Create the terminology registry** with all collision entries.
12. **Implement CI checks** for claim state validation, evidence requirements, and naming validation.
13. **Link to existing DOI-backed records** as provenance anchors.

### Long-term (for the framework to advance)

14. **Run large-scale replication** (>10,000 samples) to upgrade CT-002 from OBSERVED to SUPPORTED.
15. **Identify the symmetry** corresponding to commitment conservation (the Noether theorem gap).
16. **Develop operational criteria** for BI/AAI distinction and test them.
17. **Implement Intelligence Provenance** and compare against data provenance for predictive power.
18. **Derive Micro Evals from the ontology** and validate the derivation via CI checks.
19. **Engage with closest neighbors** — CoHSI (Hatton & Warr), Marcolli, "Lineage of Intelligence" — for potential collaboration or cross-citation.
20. **Consider a separate patent filing** for the intelligence ontology extension if patent protection is desired.

---

## Governance Footer

This review was produced in the SigRank-gtm workspace under GTM role. No canonical Commitment Theory material was modified. The Search Authority canon repository was unavailable. All claims in this review are proposals, not canonical assertions. Implementation requires owner approval, canon availability, and repository governance compliance.

**Canon rules preserved:**
- Commitment Theory contains the Conservation Law (the law is within the theory).
- The canonical law is C(T_gov(S)) = C(S).
- MO§ES™ is the enforcement architecture (proprietary core not exposed).
- Never called "McHenry's Law."
- Canonical rendering: MO§ES™. Never MO§E§.
- The harness is a proxy measurement tool, not the production enforcement implementation.
- Automated systems may not promote claims into owner-approved truth.
- Commercial packaging remains downstream from the canonical ontology.
- AAI/BI existing priority from CIVITAE ontology preserved.
