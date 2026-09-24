# Engineering challenge

A short take-home exercise for the [Python Engineer](python-engineer.md) and [Applied AI Engineer](applied-ai-engineer-retrieval.md) roles. It is not an algorithm puzzle. We want to see how you structure a system, how you handle the dull realities, and how you explain your choices.

**Time:** please spend no more than four hours. An unfinished but well-reasoned submission beats a rushed complete one.

## The task

Build a small Python service that helps a doctor prepare for a consultation.

**1. Accept a case.** `POST /cases` takes a patient's age, their reported symptoms and any known conditions, and returns an identifier.

**2. Prepare it.** For each case, assemble a short briefing for the doctor from a small set of reference notes that you supply with the project (a handful of markdown files is plenty). Every statement in the briefing must name the note it came from.

**3. Return it.** `GET /cases/{id}` returns the briefing, its sources, and how long the preparation took.

You may use any model API, or none: a stub that returns a fixed answer is acceptable if the pipeline around it is real. Tell us which you chose and why.

## What we care about

- **Structure.** Clear boundaries, readable code, sensible naming.
- **Reality.** Validation, error handling, logging, and behaviour when a dependency is slow or absent.
- **Evidence.** Tests that show the important parts work. Say what you did not test and why.
- **Honesty about limits.** A short note on what would break first at a hundred times the volume, and what you would fix before letting a doctor rely on it.
- **Safety.** This is clinical information. Tell us what you would refuse to let the system say on its own.

## What to send

A repository or an archive containing the code, a README with setup instructions of no more than ten lines, and a short design note: your choices, your trade-offs, and what you would do next with another week.

Send it to **founders@nirogiai.com**. We read every submission and reply either way, and if we take it further we will talk through your solution rather than quiz you on trivia.
