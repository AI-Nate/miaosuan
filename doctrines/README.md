# Doctrine packs — plugin spec

A doctrine pack turns a body of strategic thought into **operational lenses** the harness can select and apply. The harness never reads a book; it reads lenses.

## Layout

```
doctrines/
└── your-pack/
    ├── README.md        # what this doctrine is, when it shines, sources
    └── *.md             # lens files (any grouping: per book, per theme)
```

## Lens format

Each lens is a section in a lens file:

```markdown
## <lens-id> <name>

**源 (Source):** one-line quote + citation
**白话 (Plain):** 1–2 sentences, modern language, no mystique
**适用场景 (Triggers):** 3–5 concrete situations that should activate this lens
  — written as patterns an agent can match against real events
**所以应该 (Action template):** the shape of the action this lens produces
```

Design rules:

1. **Triggers are the product.** A lens without sharp triggers will never be selected. Write triggers against real operating situations ("a decision has been pending >3 days", "two independent sources converge on the same design"), not abstractions ("when facing difficulty").
2. **One lens = one move.** If your lens says two things, split it.
3. **3–5 lenses per file, max ~35 per pack.** A pack is a working kit, not a concordance.
4. **Plain beats classical.** The quote earns the lens its name; the 白话 and triggers do the work.

## Contributing a pack

PR with: the pack folder + one worked example in `examples/` showing your lenses applied to a (fictional) week. Packs we'd love: `stoic/` (Marcus Aurelius / Epictetus), `munger/` (inversion, incentives, lattice), `boyd-ooda/` (OODA, maneuver warfare), `clausewitz/`.
