# Software Engineer Learning Notes

A curated, phased learning path and reference notes to guide a beginner to a career in software engineering. The materials are organized by phases and topical folders with definitions, discussions, examples, and exercises (primarily Python examples).

Contents

- `software-engineer-learning-path.md` — single-page overview: roadmap, core topics, glossary, resources, projects, and career guidance.
- `Phases/` — phase-by-phase guides with explanations, exercises and example snippets.
- `Topics/` — focused topic guides. Notable folders:
  - `Topics/OOP/` — Object-Oriented Programming guide (concepts, examples, tasks).
  - `Topics/Principles/` — programming principles (SOLID, DRY, YAGNI, KISS, SoC, TDD, FP).

Quick start

1. Open this folder in VS Code.
2. Pick a phase or topic to study (Phase 0 or `Topics/OOP` recommended for beginners).
3. Run example Python files directly with Python 3.9+:

   - Create a virtual environment (optional):

     python3 -m venv .venv
     source .venv/bin/activate

   - Run a small example:

     python3 Topics/OOP/examples.md  # examples are marked for easy copy/paste into .py files

4. Run tests (if present) with pytest:

   pytest

How to use

- Read definitions and discussions to understand concepts.
- Try code examples by copying them into `.py` files and running them.
- Complete exercises in `Phases/` and `Topics/` and track progress with Git commits.

Contributing

- Keep changes focused and organized by phase/topic.
- Add a short README in any new folder describing its purpose.
- Prefer small, reviewable commits and clear commit messages.
- If adding code examples, ensure they run with Python 3 and include brief instructions.

Folder structure (high level)

- software-engineer-learning-path.md
- README.md
- Phases/
  - phase-0-mindset-and-tools.md
  - phase-1-fundamentals.md
  - phase-2-practical-engineering.md
  - phase-3-cs-foundations-and-scale.md
  - phase-4-specialization-and-career.md
- Topics/
  - OOP/
    - README.md
    - concepts.md
    - examples.md
    - tasks.md
  - Principles/
    - SOLID/
    - DRY/
    - YAGNI/
    - KISS/
    - SeparationOfConcerns/
    - TDD/
    - FP/

License

- Personal learning notes. Reuse and adapt for personal or educational use.

Contact

- Maintainer: ekimmayong (local workspace). For questions, update an issue or add a note in the relevant file.

