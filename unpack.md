---
description: Unpack an AI answer or answer a request in a low cognitive load form
---

The argument of this command is the text after the trailing separator; if there is none, the no-argument mode applies.

START_unpack

START_goal
### Goal
The reader absorbs the full meaning of an answer in a single reading pass: no return to session history, no follow-up questions, no holding earlier definitions in working memory. Reading load is reduced; the complexity of the subject is unchanged.
END_goal

START_task
### Task
Unpacking the form of an answer — existing or newly created — while semantics and the complexity level of the subject stay unchanged.

START_modes
#### Modes
- Argument present (request): fulfill the request and deliver the result directly in the target form. The reasoning runs at full register — terminology, distinctions, complete chains; only the output text undergoes unpacking.
- No argument: unpack the latest AI answer. If a quote is given, the quoted fragment is what gets unpacked.
END_modes

START_mechanisms
#### Mechanisms
1. Rhythm. Connected prose: one thought per paragraph, connectives between sentences; no telegraphic style, no scattered fragments.
2. Self-sufficiency. A term or concept gets a brief reminder from the session context at its first use — reactivating what was already given, not re-explaining from scratch.
3. Essence → details. The first block of the answer is the essence: conclusion, state, decision — briefly. Then details with the context needed to understand them. The first block serves as the opening.
END_mechanisms

START_invariants
#### Invariants
1. Semantics carry over one-to-one: nothing lost, nothing added. Exact values — identifiers, numbers, paths, commands — are copied verbatim. *Rationale: paraphrasing an exact value distorts the fact; form does not restore content.*
2. The complexity of the subject is a constant. *Rationale: lowering the entry level collapses terminology and distinctions — content degrades along with form.*
3. Expansion limit: volume grows only where explicitness reduces load. *Rationale: volume is itself a source of load; limitless expansion reproduces the original problem.*
END_invariants

START_form
#### Form
- Sufficient typography: headings and lists only where they aid reading; the amount of structure is proportional to the length of the answer. Prose comes first.
- No narrative constructions about the answer itself: prologues, "let's break this down", closing courtesies. There is no separate opening — the first block with the essence does that job.
- The output language is Russian, regardless of the source language.
- The object is chat text. Code, paths, and files are not touched.
END_form

END_task

START_completion
### Completion
- Success: terminology, distinctions, and caveats are fully preserved — nothing lost, nothing added on your own; exact values unchanged; every addition is justified by load reduction; the answer reads in a single pass.
- Form: a single output; drafts and variants are not emitted.
- Dead end: nothing to unpack (input empty; the latest answer is only code or tool results) — do not emit an empty form, request the input.
END_completion

END_unpack

---
$ARGUMENTS
