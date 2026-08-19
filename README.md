# QCAA Physics — Units 3 & 4 flashcards

A spaced-repetition flashcard deck for the Physics 2025 v1.3 General senior syllabus.
Single HTML file, no build step, no account, no server.

**278 cards**, covering:

| Section | Cards |
|---|---:|
| Unit 3 — Gravity and motion | 62 |
| Unit 3 — Electromagnetism | 67 |
| Unit 4 — Special relativity | 43 |
| Unit 4 — Quantum theory | 38 |
| Unit 4 — The Standard Model | 41 |
| Data analysis and uncertainty | 27 |

19 are diagram cards drawn as inline SVG — inclined-plane free-body diagrams, projectile
components, field lines, the three hand rules, flux through a coil, the photoelectric
graph, hydrogen energy levels, particle interaction diagrams, accuracy-versus-precision
targets, and min/max trendlines through error bars.

## Scope

Cards were written against the Unit 3 and Unit 4 **science understanding** subject matter,
plus the data-analysis and uncertainty skills from the science inquiry skills list
(pp. 12–13). Every card maps to a dot point; every assessable dot point has at least one
card.

Deliberately **excluded**:

- **Science as a Human Endeavour.** Internal-assessment only, and not examinable.
- **IA process skills** — writing research questions, designing investigations, risk and
  ethics, referencing conventions. These are things students *do*, not things they recall.
- **Unit 1 and Unit 2 content**, even where it underpins Units 3 and 4.
- **Numerical constants.** Students have the QCAA formula and data book in every paper, so
  cards name constants rather than asking students to memorise values.

## Hand rule conventions

Stated consistently throughout, since this is where decks usually contradict themselves:

- **Right-hand grip rule** — magnetic field produced by a current (straight wire, solenoid polarity).
- **Fleming's left-hand rule** — motor effect: force on a current or moving positive charge in a field.
- **Fleming's right-hand rule** — generator effect: direction of induced current.
- **Negative charges** — reverse the direction the current finger points. Do not reverse the
  current finger *and* the resulting force; that cancels out and gives the wrong answer.

## Using it

Open the page. Space reveals the answer, `1` marks it missed, `2` marks it correct.

Scheduling is a five-box Leitner system with review intervals of 0, 1, 3, 7 and 16 days.
A missed card drops to Box 1 and reappears in the same session. The streak counter tracks
consecutive days with at least one review.

Students can flag any card as wrong or confusing, then export their flagged list via the
share sheet or clipboard to send to a teacher.

## Hosting

Serve `index.html` from any static host. **Link to it directly — do not embed it in an
iframe.** Browsers partition or block third-party `localStorage`, so an LMS embed will look
fine and then silently lose every student's progress between sessions.

Uploading the file as an LMS attachment usually serves it as a download rather than a page,
for the same reason: host it, then link.

## Privacy

Progress is written to `localStorage` in the student's own browser under the key
`qcaa.physics34.deck.v1`. Nothing is transmitted, collected, or shared. There is no
analytics, no telemetry, and no back end.

The page loads KaTeX and IBM Plex from public CDNs (jsdelivr, Google Fonts), which see a
request from the visitor's IP as they would for any web page. If the CDN is unreachable —
some school networks block it — maths falls back to a Unicode renderer and the deck stays
usable.

Progress is per-browser and per-device: a student using a library PC and a phone has two
separate sets of boxes, and clearing site data resets them.

## Editing the deck

Cards live in a `<script id="deck" type="text/plain">` block near the bottom of the file,
one per line, pipe-delimited:

```
topic|type|question|answer|watch-for note|inline SVG
```

`topic` is one of `g e r q s d`. `type` is `qa`, `cloze`, `calc` or `svg`. The last two
fields are optional. Cloze deletions are marked `[[like this]]`. Maths is LaTeX between
single `$` delimiters.

Card identity is an FNV-1a hash of the question text, not the line position, so cards can
be added, removed or reordered without disturbing students' saved progress. Editing a
question's wording changes its identity and resets that one card — editing the *answer* is
free.

Stored progress for cards that no longer exist is pruned automatically on load.

## Licence

Application code: MIT.

Card content is derived from the Physics 2025 v1.3 General senior syllabus,
© State of Queensland (QCAA) 2026, [www.qcaa.qld.edu.au/copyright](https://www.qcaa.qld.edu.au/copyright),
used under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0). Retain that attribution
in any copy or adaptation. See `LICENSE` for the full notice.

The QCAA has not endorsed, reviewed, or been involved in this resource.

## Accuracy

Cards were drafted with AI assistance from the syllabus text, reconciled against the dot
points, and read in full before release. Errors are still possible — check anything before
you put it in front of a class, and use the in-app flag button to collect student reports.
