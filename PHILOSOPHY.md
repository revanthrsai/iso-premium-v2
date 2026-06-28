# The ISO 20022 Academy — Teaching Philosophy

> **The one law everything else obeys:**
> **Every lesson must begin with a human question, not a technical concept.**

This document is the academy's constitution. It is not marketing copy and it is
not a style guide — it is the contract every lesson is measured against. If a
lesson and this document disagree, the lesson is wrong.

Read this before writing or reviewing any content.

---

## 1. Why we teach ISO 20022

We are not here to help someone pass a migration deadline. Deadlines expire.

We teach ISO 20022 because it is the closest thing humanity has ever built to a
**universal language for trust and value** — the rules by which money moves
between strangers who will never meet, across borders, currencies, and time
zones, and still arrives intact. Behind a payment that *looks* instant on a phone
screen sits five thousand years of people solving the same problem over and over:
*how do I know the value I'm owed will actually reach me?*

ISO 20022 is the current answer. Our job is to make a learner *understand that
answer* — not memorize its tags. When they finish, they should see the financial
system the way the people who built it do: as a chain of human problems, each
solved just well enough to expose the next one.

A learner who only memorizes `pacs.008` forgets it in a week. A learner who
understands *why money needs a `pacs.008`* never unlearns it.

---

## 2. What a learner should feel

In this exact order:

1. **Curiosity first.** Every lesson opens with a question they actually want
   answered. The feeling is *"huh, I never thought about that."*
2. **Recognition second.** *"Oh — that's a problem I've sort of felt myself."*
   (Their card got declined. A transfer "pending" for two days. A wrong name on a
   wire.) We connect the abstract to something they've lived.
3. **Competence third.** *"I get it now — and I could explain it to someone
   else."* Competence is the payoff, never the entry fee.

What a learner must **never** feel: **overwhelmed**. Confusion is not rigor.
If a lesson makes someone feel stupid, the lesson failed, not the learner. Every
cryptic tag, every nested structure, every acronym is a tax on attention — and we
spend that attention budget only on *real understanding*, never on decoding
jargon we could have explained in plain words.

*(In the language of the research: minimize **extraneous load** — cryptic syntax,
unexplained abbreviations — so the learner's full attention goes to **germane
load** — the actual idea. We never make them parse `CdtrAgt` and grasp interbank
routing in the same breath.)*

---

## 3. The promise

We make the learner exactly one promise, and we keep it without exception:

> **You will never be shown a tag before you've been shown the human problem it
> solves.**

XML is the *last* thing a learner meets in any lesson, never the first. A tag is
only ever revealed as *"here's how the world happens to write down the thing you
already understand."* Syntax is a costume the meaning wears — and we always
introduce the problem before the costume.

---

## 4. Our voice

The History page already found it. Every other page should read like **the next
scene of the same film**, never a tonal reset into a textbook.

- **Cinematic and real.** We tell stories about real money in motion — a payroll
  run, a stuck wire, a midnight treasury sweep — not "the standard specifies
  that…"
- **Second-person and present.** *"A payroll run for five thousand people just
  left the building. Right now, each payment is sitting in a queue you've never
  had to think about — until one of them bounces."* The learner is inside the
  moment, not reading a report about it.
- **Plain before precise.** Say the everyday thing first, the exact term second:
  *"the receiving bank — the **Creditor Agent** —"*. Never the reverse.
- **Confident, not academic.** Short sentences. Concrete nouns. We earn trust by
  being clear, not by sounding complex. If a sentence needs a glossary lookup to
  parse, rewrite the sentence.
- **Real over invented.** Warmth comes from real stakes, not invented
  personalities. We don't need a recurring cast of characters to make money feel
  human — a real payroll run for five thousand people, a real wire that bounced
  off a sanctions filter, already has stakes built in. No emoji, no jokes, no
  storyline. The scenario is doing the work, not a personality.

> **The voice test:** read any paragraph aloud. If it sounds like documentation,
> it's wrong. If it sounds like a good engineer walking a colleague through
> something genuinely interesting, it's right.

---

## 5. What makes us different from documentation

Documentation answers **"what is this field?"**
We answer **"why does this field exist — and who got hurt before it did?"**

| Documentation | The Academy |
|---|---|
| Starts with the structure | Starts with the human question |
| Lists what a message contains | Tells you why the message had to be invented |
| Treats XML as the subject | Treats XML as the *last step*, a serialization of meaning |
| Defines `Debtor` | Shows you a real payroll run, then names what just happened |
| Complete | **Understandable** |

Anyone can read the ISO spec. Almost no one finishes it understanding *why*. That
gap is the entire reason this academy exists.

---

## The Lesson Spine

Every unit of knowledge in the academy — a domain, a single message, a glossary
term, a history chapter — is taught in this **fixed nine-beat order**. This is the
core law made operational. Do not reorder it. Do not let a later beat leak into an
earlier one (no tags in beat 1, no XML before beat 7).

| # | Beat | What it must do |
|---|------|-----------------|
| 1 | **The Human Question** | One sentence a non-banker would actually ask out loud. Contains **no** tag, acronym, or the words *XML / schema / message*. |
| 2 | **Who feels this** | Name the role in pain *before* the solution existed, and what it cost them. |
| 3 | **The Story** | A real, concrete scenario — drawn from the Working Set below — playing out the problem with real institutional roles (a payroll provider, a correspondent bank, a treasury desk), not abstract entities. |
| 4 | **How the world solved it** | The business process and the people in it, in plain English. Diagrams in business terms, not tags. |
| 5 | **How ISO *models* it** | The semantic roles — Debtor, Creditor, Agent, Amount — as *concepts*. Still no tags. |
| 6 | **The message(s)** | Which message carries this, named in business terms first (*"the bank-to-bank credit transfer — `pacs.008`"*). |
| 7 | **The real XML** | *Only now.* Shown explicitly as "one way to write down beat 5." Tags are translated inline on first sight. |
| 8 | **What breaks** | A concrete, real failure — truncated name flags a sanctions match, a missing TARGET2 codeword, a bad UETR. Specific, never hand-wavy. |
| 9 | **You can now…** | One concrete earned skill, stated plainly (*"You can now read a `pacs.008` and say who's paying whom"*), plus 2–4 links to related ideas. |

### The acceptance test (run on every lesson, every time)

> Read **beat 1** aloud.
> - Does it contain a tag name? **Fail.**
> - Does it contain an acronym? **Fail.**
> - Does it contain the word *XML*, *schema*, or *message*? **Fail.**
> - Would a working engineer actually ask it out loud? If not, **rewrite.**
>
> Then check: does any beat **before 7** show raw XML? If yes, **fail** — move it.

A lesson that cannot pass this test does not ship.

---

## Canon: The Working Set of Real Use Cases

Every story in the academy is drawn from a small, fixed set of real-world
scenarios — not invented characters, not a continuing storyline. Reusing the same
five scenarios across levels gives the learner continuity (they recognize a
scenario faster the second time) without needing a fictional cast to manufacture
that familiarity. These five are not arbitrary — they are exactly the five Case
Studies in the Library's 500 level, which means every earlier lesson is, in
effect, foreshadowing one of those capstones.

| Use case | Signature moment | Best for | Messages / concepts | Failure variant (400 Exceptions) |
|---|---|---|---|---|
| **Customer Transfer** | A customer pays her landlord $1,200. It takes one tap. It takes three institutions. | 100 Fundamentals — what is a payment, payment lifecycle, clearing vs settlement | `pain.001` → `pacs.008` → `camt.054` | Malformed account number → **Reject** |
| **Payroll** | A payroll provider pays five thousand employees at 6 a.m. on the 1st. One of them bounces. | 200 Architecture — batch processing, payment hub; 300 `pain` family | Bulk `pain.001`, status reporting `pacs.002` | An employee's account is closed → **Return** |
| **Cross-border Payment** | A worker abroad sends $400 home. It crosses two currencies, three banks, and one sanctions filter before it lands. | 300 `pacs` family; History — why legacy formats caused real failures | `pacs.008`, `pacs.009 COV`, FX conversion | Beneficiary name truncated, trips a sanctions match → **Reject** |
| **Treasury** | A multinational sweeps every subsidiary account into one pool, every night, before anyone wakes up. | 200 Architecture — payment hub/switch; 300 `camt` family | `camt.053`/`054` statements, liquidity management | A sweep posts to the wrong subsidiary → **Reversal** |
| **End-to-End Payment Flow** | Follow one payment from the moment it's initiated to the moment it's reconciled — and the one place it can still go wrong. | 500 Case Studies (capstone); Message Lifecycle | The full chain, every message type above | A payment goes missing mid-route → **Recall / Investigation** |

### Rules for using the working set

- **Pull from this table first.** A learner who already met the Payroll scenario
  in 200 Architecture recognizes it faster when it resurfaces in 400 Exceptions —
  that's the continuity benefit, without a fictional storyline.
- **Use real institutional roles and realistic specifics** — actual currencies,
  believable transaction sizes, real timeframes. Never a generic placeholder like
  "Company A" or "User X."
- **It's fine to introduce a new scenario** if none of the five genuinely fits a
  lesson — but add it to this table immediately so it doesn't become an orphan
  one-off nobody else can reuse.
- **No persistent personalities, relationships, or storyline** beyond what's
  strictly needed to make a scenario legible. We are not building a series — we
  are showing real work.
- **Each signature moment is the beat-1 hook.** It's written to earn a working
  engineer's curiosity, not a general audience's sentimentality — keep new
  signature moments in that register.

---

## The single sentence to remember

If you forget everything else in this document, keep this:

> **Introduce the real scenario before the syntax. A real payment, a real
> failure, a real institution — the tag comes last, if at all.**