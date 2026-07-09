# Reading Methodologies by Book Category

Loaded during Phase 0 (new book initialization). Classify the book, then recommend the matching methodology BEFORE generating the study plan. The chosen approach shapes: reading order, pace, pre-reading question style (Phase 1), ingest focus (Phase 2), and what "mastery" means (Phase 3).

## Step 1: Classify

Determine category from title, author, table of contents, and the user's stated goal. If ambiguous, ask the user for the TOC or back-cover blurb. A book can be hybrid (e.g. pop-science memoir) — pick the dominant type, borrow tactics from the secondary.

Always start any new book with **inspectional reading** (검시 독서 / inspectional reading, per Adler): 15–30 min skim of TOC, preface, chapter openings/closings, index. This both confirms the category and gives the skeleton for `study-plan.md`.

## Step 2: Apply the matching methodology

### 1. Practical / How-to (business, self-help, productivity, methodology)
- **Goal**: change behavior, not collect ideas. A practical book is only "read" when something is applied.
- **Order**: non-linear is fine. After the skim, prioritize chapters that hit the user's Phase-0 problem; deprioritize padding chapters (many practical books are 2 ideas + 10 case-study chapters).
- **Pace**: fast through anecdotes, slow on the actual rules/frameworks.
- **Pre-reading questions**: "What would you do in [user's real scenario] today, before reading the author's answer?"
- **Ingest focus**: `models/` (the prescriptions) over `quotes/`. Every chapter ingest must answer: "What will the user do differently?"
- **Mastery**: Phase 3b practice task is mandatory and must use the user's real work context.

### 2. Theoretical / Expository (psychology, economics, sociology, pop-science)
- **Goal**: rebuild the author's argument chain — claims, evidence, and how concepts connect.
- **Order**: linear; later chapters assume earlier concepts.
- **Pace**: steady; slow down where a new core concept is defined.
- **Pre-reading questions**: prediction-style — "What do you expect the author will argue causes X?"
- **Ingest focus**: `concepts/` + `cases/` (the experiments/evidence backing each claim). Map claim → evidence explicitly.
- **Mastery**: user can state the claim AND the evidence for it, and name one limitation.

### 3. Technical / Science & Math (textbooks, engineering, programming)
- **Goal**: operational ability — can DO the thing, not just describe it.
- **Order**: linear within prerequisite chains; use the skim to map which chapters the user's goal actually requires.
- **Pace**: slowest of all categories. Work examples/exercises by hand; never let a derivation or code sample pass unexecuted.
- **Pre-reading questions**: "Try [small exercise] with what you know now."
- **Ingest focus**: `models/` with worked examples; record the user's own solved exercises in `cases/`.
- **Mastery**: solve a novel problem, not restate the text.

### 4. History / Biography
- **Goal**: causation and patterns, not date recall.
- **Order**: linear (narrative), fast first pass.
- **Pace**: fast; do not stop to memorize particulars.
- **Pre-reading questions**: "Given the situation at the end of last chapter, what decision would you have made?"
- **Ingest focus**: `cases/` (decisions + consequences) and cross-book patterns; timeline in `models/` if useful.
- **Mastery**: explain why an outcome happened and what generalizes to the user's context.

### 5. Philosophy / Big-idea essays
- **Goal**: dialogue with the author — identify the question being asked, the answer given, and where the user agrees/disagrees.
- **Order**: linear, but expect to re-read key passages.
- **Pace**: slowest per page; short reading sessions are fine.
- **Pre-reading questions**: ask the user the chapter's core question BEFORE reading, so they form their own position first.
- **Ingest focus**: `questions/` is the primary output (disagreements, tensions); `quotes/` for load-bearing passages.
- **Mastery**: state the author's position, the strongest objection, and the user's own position.

### 6. Imaginative Literature (fiction, poetry, drama)
- **Goal**: experience first, analysis second. Do NOT dissect on first pass.
- **Order**: linear, immersive, as few interruptions as possible.
- **Pace**: as fast as comprehension allows; ingest per PART or on finish, not per chapter.
- **Pre-reading questions**: skip or keep to one light question; heavy questioning kills the experience.
- **Ingest focus**: themes, character arcs, striking passages (`quotes/`). Skip the mastery rubric's "Applied" criterion.
- **Mastery**: relaxed — a good conversation about what the book meant replaces Socratic testing. No spaced-repetition scheduling unless the user asks.

### 7. Reference / Manual (dictionaries, API docs, cookbooks)
- **Goal**: retrieval, not coverage. Never read cover-to-cover.
- **Method**: skim the organization once, then drive entirely by the user's live problems. Ingest only entries actually used. No study plan table; `query` sub-command is the main interface.

## Step 3: Record & adapt

1. Write the category AND chosen approach into `meta.md` (**Category** and **Reading Approach** fields).
2. Reflect the approach in `study-plan.md` (e.g. chapter subset for practical books, part-level rows for fiction).
3. In every later phase, honor the approach — e.g. don't run full Socratic mastery tests on a novel, don't let a technical book pass without worked exercises.
