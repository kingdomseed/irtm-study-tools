# IRTM Study Tools

Interactive study tools for **Information Retrieval & Text Mining** (IRTM), a graduate course in the M.Sc. Computational Linguistics program at the University of Stuttgart.

**Live at [irtm.binaryloom.io](https://irtm.binaryloom.io)**

---

## Tools

### Exam Drill Cards

23 exam-style questions grouped by topic with fully worked solutions. Covers the core IRTM syllabus:

- Boolean retrieval & inverted indexes
- TF-IDF weighting & cosine similarity
- Index construction (BSBI, SPIMI, MapReduce)
- Index compression (variable-byte, gamma codes)
- Permuterm & k-gram wildcard indexes
- Edit distance (Levenshtein & Damerau-Levenshtein)
- Evaluation metrics (precision, recall, MAP, F1)
- Probabilistic retrieval (BM25)
- PageRank & web search
- Text classification (Naive Bayes, kNN)
- Clustering (k-means, silhouette coefficient)
- Relevance feedback & query expansion

Questions are drawn from past exams (WS19/20 through WS24/25) with frequency ratings so you know what comes up most often.

### Permuterm Index Visualizer

Step-through animation showing how permuterm indexes handle wildcard queries. Two phases:

1. **Building** — append `$` sentinel, generate all character rotations, sort into a B-tree-style index
2. **Querying** — transform a wildcard query (e.g., `t*o`) by rotating until `*` is at the end, then do a simple prefix lookup

Includes presets from past exam questions (WS21/22, WS24/25) and a teaching example.

### Edit Distance Visualizer

Step-through matrix construction for both Damerau-Levenshtein and standard Levenshtein distance. Features:

- **Back-calculation highlighting** — source cells are color-coded with arrows and cost badges showing exactly which cells fed into each computation
- **Operation breakdown** — side panel shows all candidate operations (match, substitute, insert, delete, transpose) with their values
- **Mode toggle** — switch between Damerau-Levenshtein (with transpositions) and standard Levenshtein to see how results differ
- Presets from past exams (WS19/20, WS24/25) and teaching examples

---

## Course Context

IRTM is taught at the [Institute for Natural Language Processing (IMS)](https://www.ims.uni-stuttgart.de/) at the University of Stuttgart. The course covers the theory and practice of information retrieval and text mining, from classical Boolean and vector space models through modern probabilistic ranking and web search.

This tool set was built as exam preparation for the Winter semester 2025/26 exam.

## Tech

Pure HTML/CSS/JavaScript — no build step, no dependencies. Each tool is a single self-contained `.html` file. Animations use the Web Animations API. Deployed to Cloudflare Pages.

## Sister Project

Methods in Computational Linguistics flashcards at [study.binaryloom.io](https://study.binaryloom.io)
