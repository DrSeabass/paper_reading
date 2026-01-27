Rolling Annotated Bibliography Sorted by Topic

# Directory Structure
Each top‑level folder represents a topic, project, or reason for reading.
Inside each topic folder:
```
topic_or_reason/
│
├── summary.md          # High‑level overview synthesizing papers in this topic
├── paper_title_1.md      # Focused notes on a single paper
└── paper_title_1.pdf     # (Optional) The PDF of the paper for reference
├── paper_title_2.md      # Focused notes on a single paper
└── paper_title_2.pdf     # (Optional) The PDF of the paper for reference
```

This structure keeps related works together, supports incremental reading, and makes resurfacing prior insights easy.

# File Types & Conventions

## summary.md
A high‑level overview for the topic folder. Often includes:

* A short description of why the topic matters
* Bullet‑point takeaways across papers
* Links to individual paper notes
* Open questions or research directions

Useful when returning to a research area after time away.

## paper_title.md
A dedicated note for a single paper.

## paper_title.pdf
Optional, but recommended if:

* You annotate PDFs externally
* You want offline availability
* You prefer to keep everything in one topic folder

# Search & Cross‑Referencing
Inside Obsidian, papers can be linked to:

* Research project folders (e.g., [[research_projects/TOPIC]])
* Meeting notes
* Experiments
* Hypothesis files

This creates a lightweight knowledge graph that shows how your reading informs your work.
Some of the links in this repository may look dead to you unless you clone the mentioned repositories into the correct location.  Notes on intended structure are in the journal repository.

# Workflow

* When you start reading a paper
  * Create paper_title.md in the relevant topic folder
  * Add the PDF if you plan to annotate or reread it
* As you read
  * Fill in summary sections incrementally
  * Add cross‑links to research ideas, hypotheses, or experiments
* When you finish a cluster of papers
  * Update summary.md to synthesize the set
* When a new project starts
  * Decide if a new topic folder is needed for its reading queue
  * Create it if so

