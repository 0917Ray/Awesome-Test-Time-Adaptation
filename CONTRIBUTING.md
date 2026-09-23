# Contributing

Thank you for helping improve Awesome Test-Time Adaptation. Contributions can
add papers, correct metadata, repair links, or improve the taxonomy.

## Before opening a pull request

Please check that the proposed work:

- uses information available at deployment time to adapt a model, its
  statistics, prompts, memory, or predictions;
- is a published paper or a substantive public preprint;
- is not already listed under another year or name;
- links to the primary paper page and, when available, the official code or
  project page; and
- has working links and accurate venue/year metadata.

## Entry format

Add papers in reverse chronological order within the correct year in
`README.md`. Then add a link under one or more matching sections in
`TOPICS.md`. Use this template and keep the explanation to one sentence:

```markdown
- **METHOD** - *Full Paper Title*. Venue Year. `Method family`
  [![Paper](https://img.shields.io/badge/Paper-arXiv-b31b1b?logo=arxiv&logoColor=white)](PAPER_URL)
  [![Code](https://img.shields.io/badge/Code-GitHub-181717?logo=github)](CODE_URL)
  - One sentence explaining the paper's main test-time adaptation idea.
```

Use a ⭐ only for a foundational paper or a broadly useful starting point.
Please do not mark a paper solely because you authored it.

## Pull request checklist

- [ ] I searched the README for duplicate titles and method names.
- [ ] I verified the title, venue, year, and links.
- [ ] I used the existing entry format and method tags.
- [ ] I added a concise, neutral description rather than promotional text.
- [ ] I kept the pull request focused on related changes.
- [ ] I added the paper to at least one relevant topic in `TOPICS.md`.

By contributing, you agree that your contribution is made available under the
repository's [CC0 1.0 Universal](LICENSE) dedication.
