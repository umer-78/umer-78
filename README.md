# Umer Hashmi

Software engineer. I build security tools, machine learning projects and
applications. Every repository below has a README with real output, a test
suite, and CI that builds it on a clean machine.

**Portfolio: [umer-78.github.io](https://umer-78.github.io/)**

---

## Security & networking

| Project | What it does |
| --- | --- |
| [password-strength-checker](https://github.com/umer-78/password-strength-checker) · [demo](https://umer-78.github.io/password-strength-checker/) | Offline password analyzer: entropy, leetspeak, keyboard walks, dates, passphrase scoring, and a `--min-score` CLI gate. |
| [log-sentinel](https://github.com/umer-78/log-sentinel) · [demo](https://umer-78.github.io/log-sentinel/) | Finds SSH brute-force, password spraying and success-after-failure logins in Linux auth logs. |
| [file-integrity-monitor](https://github.com/umer-78/file-integrity-monitor) · [demo](https://umer-78.github.io/file-integrity-monitor/) | SHA-256 baselines with HMAC signing, so a tampered *baseline* is caught too. Watch mode included. |
| [security-headers-scanner](https://github.com/umer-78/security-headers-scanner) · [demo](https://umer-78.github.io/security-headers-scanner/) | Grades a site's HTTP security headers and cookies A–F, with the exact header line that fixes each finding. |
| [regex-engine](https://github.com/umer-78/regex-engine) · [demo](https://umer-78.github.io/regex-engine/) | A regex engine with four engines over one pattern, so catastrophic backtracking can be measured. On `(a+)+b` the backtracking matcher takes 2^(n+4) − (n+9) steps where the Thompson NFA takes 30n − 25 — and Python's own `re`, a backtracking engine, takes 25 seconds at n=28. |
| [subnet-calculator](https://github.com/umer-78/subnet-calculator) · [demo](https://umer-78.github.io/subnet-calculator/) | IPv4 subnetting, equal split and VLSM in the browser. The maths module has no DOM in it, so it is unit tested. |

## Machine learning & AI

| Project | What it does |
| --- | --- |
| [llm-gateway](https://github.com/umer-78/umer-78-llm-gateway) | Self-healing gateway in front of several LLM providers: circuit breakers kept in Redis, failover by request class, hedged requests and a queue that waits out outages, with cost per tenant and feature. Answered 92.2% of interactive requests through scripted outages, against 74.4% when calling one provider directly. |
| [gradient-boosting](https://github.com/umer-78/gradient-boosting) · [demo](https://umer-78.github.io/gradient-boosting/) | Gradient boosting written from scratch: histogram trees, Newton leaf values, early stopping. Every gradient is checked against finite differences, and it shows gain importance ranking a planted noise column above a real predictor while permutation importance scores it zero. |
| [recommender-engine](https://github.com/umer-78/recommender-engine) · [demo](https://umer-78.github.io/recommender-engine/) | Popularity and random baselines, item-item CF, matrix factorisation and BPR on a temporal split. Demonstrates that rating-trained factorisation ranks worse than random, and the same model trained with a pairwise loss ranks 13× better. |
| [anomaly-detection](https://github.com/umer-78/anomaly-detection) · [demo](https://umer-78.github.io/anomaly-detection/) | Statistical detectors and an isolation forest for metrics, with a random detector shipped in the box to show how far point-adjusted F1 flatters a detector — pure noise reaches 0.46 on it, beating the isolation forest's honest 0.42. |
| [image-toolkit](https://github.com/umer-78/image-toolkit) · [demo](https://umer-78.github.io/image-toolkit/) | Image processing from scratch in NumPy: convolution kept distinct from correlation, a separable Gaussian doing 50 multiplies per pixel instead of 625 (14.5× faster in the benchmark) and identical to 1e-13, Otsu thresholding and Canny-style edges. |
| [neural-network-from-scratch](https://github.com/umer-78/neural-network-from-scratch) · [demo](https://umer-78.github.io/neural-network-from-scratch/) | Feed-forward network in pure NumPy. Every hand-derived gradient is checked against a numerical estimate — the test fails if the calculus is wrong. |
| [rag-document-qa](https://github.com/umer-78/rag-document-qa) · [demo](https://umer-78.github.io/rag-document-qa/) | Question answering over your own documents: structure-aware chunking, BM25 + TF-IDF hybrid retrieval, cited answers, no API key. |
| [sentiment-analyzer](https://github.com/umer-78/sentiment-analyzer) · [demo](https://umer-78.github.io/sentiment-analyzer/) | Naive Bayes written from scratch and scored beside scikit-learn's on the same data, with negation handling and per-prediction explanations. |
| [customer-churn-prediction](https://github.com/umer-78/customer-churn-prediction) · [demo](https://umer-78.github.io/customer-churn-prediction/) | Three models and a majority-class baseline compared on one split, with PR-AUC as the headline metric because missing a churner is the costly error, plus a model card and a scoring CLI. |
| [ml-model-serving-api](https://github.com/umer-78/ml-model-serving-api) · [demo](https://umer-78.github.io/ml-model-serving-api/) | FastAPI service for a scikit-learn model: validation, model versioning, rollback, health and metrics endpoints. |

## Data & analytics

| Project | What it does |
| --- | --- |
| [route-planner](https://github.com/umer-78/route-planner) · [demo](https://umer-78.github.io/route-planner/) | Shortest and fastest routes over a 1,600-intersection network: Dijkstra, A* and bidirectional search sharing one implementation. The heuristic's admissibility is tested against the real network, and a heuristic weighted 1.2 expands *more* nodes than an unweighted one. |
| [text-search](https://github.com/umer-78/text-search) · [demo](https://umer-78.github.io/text-search/) | A search engine built from the index up in pure Python: positions, BM25, phrase and boolean queries, the Porter stemmer and typo tolerance. Uses the clamped idf because the textbook BM25 form measures −1.4351 on a term in 10 of 12 documents, penalising a document for containing the query. |
| [mini-sql-engine](https://github.com/umer-78/mini-sql-engine) · [demo](https://umer-78.github.io/mini-sql-engine/) | A SQL engine written from scratch (tokenizer, recursive-descent parser, executor) running joins, grouping, aggregates, UNION and CASE over CSV files, plus INSERT, UPDATE and DELETE that only reach the files when saved, with three-valued NULL logic and errors that point at the offending character. |
| [timeseries-forecasting](https://github.com/umer-78/timeseries-forecasting) · [demo](https://umer-78.github.io/timeseries-forecasting/) | Baselines, exponential smoothing and rolling-origin backtesting with no dependencies. MASE is scaled by the training window, and a test proves no fold ever sees data past its own origin. |
| [sales-insights](https://github.com/umer-78/sales-insights) · [demo](https://umer-78.github.io/sales-insights/) | pandas analysis with an audit trail: every row dropped in cleaning is counted and explained. Cohort retention, RFM segmentation, seasonality. |
| [ta-indicators](https://github.com/umer-78/ta-indicators) · [demo](https://umer-78.github.io/ta-indicators/) | Dependency-free technical indicators in strict TypeScript, checked against published worked examples. |

## Applications & services

| Project | What it does |
| --- | --- |
| [diffkit](https://github.com/umer-78/diffkit) · [demo](https://umer-78.github.io/diffkit/) | Diff, patch and three-way merge in Go with no dependencies. Its unified output is checked against GNU diff rather than only round-tripped through its own parser, and it measures what the textbook LCS table costs: 158× the time and 59× the memory of Myers' algorithm for the same eleven edits. |
| [pebble-lang](https://github.com/umer-78/pebble-lang) · [demo](https://umer-78.github.io/pebble-lang/) | A small programming language built end to end in Python: lexer, Pratt parser, static scope resolver and tree-walking interpreter, with closures and a REPL. Running the same program with `--no-resolve` reproduces the closure late-binding bug the resolver removes, so the difference is a measurement rather than a claim. |
| [bank-ledger-csharp](https://github.com/umer-78/bank-ledger-csharp) · [demo](https://umer-78.github.io/bank-ledger-csharp/) | Append-only account ledger in C#/.NET 8. Money is `decimal`, entries are never edited, and `audit` replays every entry from zero to prove each balance still agrees with its entries. |
| [kv-store](https://github.com/umer-78/kv-store) · [demo](https://umer-78.github.io/kv-store/) | A log-structured key-value store in Go: write-ahead log, SSTables, bloom filters and compaction. Reading an absent key is 50× faster than a present one: the bloom filter eliminates 82% of negative lookups without a disk read. A crash mid-write loses only what was never acknowledged. |
| [loadgun](https://github.com/umer-78/loadgun) · [demo](https://umer-78.github.io/loadgun/) | HTTP load testing in Go: worker pool, rate cap, nearest-rank percentiles and a latency histogram, exiting non-zero so it works as a CI gate. |
| [url-shortener-go](https://github.com/umer-78/url-shortener-go) · [demo](https://umer-78.github.io/url-shortener-go/) | URL shortener in Go: JSON API, custom codes, expiring links, atomic visit counting, single static binary, distroless image. |
| [inventory-management-system](https://github.com/umer-78/inventory-management-system) · [demo](https://umer-78.github.io/inventory-management-system/) | Stock control on a movement-ledger design: stock on hand is derived, never a field that can drift. Suppliers, purchase orders, valuation, reorder alerts. |
| [project-tracker](https://github.com/umer-78/project-tracker) · [demo](https://umer-78.github.io/project-tracker/) | Team project management: kanban with drag and drop, sprints, burndown, workload and role-based permissions. |
| [task-board](https://github.com/umer-78/task-board) · [demo](https://umer-78.github.io/task-board/) | Kanban in React and TypeScript where every drag has a keyboard equivalent, and cards animate with Motion. |
| [ui-lab](https://github.com/umer-78/ui-lab) · [demo](https://umer-78.github.io/ui-lab/) | Six animation patterns for React with Motion — shared layout, enter/exit, drag, springs, height auto, scroll progress — each one file, each with a keyboard route and reduced-motion support. |
| [weather-now](https://github.com/umer-78/weather-now) · [demo](https://umer-78.github.io/weather-now/) | Weather dashboard on the keyless Open-Meteo API. The hourly strip starts at the current hour, not at midnight. |
| [coinvantage](https://github.com/umer-78/coinvantage) · [demo](https://umer-78.github.io/coinvantage/) | Installable crypto markets site: live prices, charts, signals, calculators and an on-device forecast that reports its measured accuracy. No API keys, never trades, and wallet connection is read-only. |

## Games & interactive

| Project | What it does |
| --- | --- |
| [GD_PROJECT](https://github.com/umer-78/GD_PROJECT) · [demo](https://umer-78.github.io/GD_PROJECT/) | Unity 3D maze game: five hand-built levels, NavMesh guards that check line of sight before firing, moving obstacles that damage the player, and coins that unlock the exit door. Playable in the browser. |
| [snake-game](https://github.com/umer-78/snake-game) · [demo](https://umer-78.github.io/snake-game/) | Snake on a canvas with the rules separated from the rendering and unit tested: queued turns mean two fast key presses can't fold the snake into itself. |

---

## How I work

- **Tests are part of the deliverable.** Logic goes in modules with no I/O and no
  DOM, so it can be tested directly rather than through the UI.
- **READMEs show real output.** The numbers and terminal blocks in my READMEs are
  pasted from actual runs, not written from memory.
- **CI builds it on a clean machine**, because "works here" is not a claim.
- **Derived state over stored state.** Balances, stock levels and scores are
  computed from their history, so they cannot silently drift.

## Tools

**Languages** Python · JavaScript · TypeScript · C# · Go · SQL\
**ML & data** NumPy · pandas · scikit-learn · Matplotlib\
**Web** FastAPI · React · Vite · Node · Tailwind CSS · Motion (Framer Motion)\
**Data stores** SQLite · PostgreSQL\
**Other** Docker · GitHub Actions · Unity · pytest · xUnit · Vitest\
**AI tooling** 21st.dev MCP · UI UX Pro Max

## Reach me

- GitHub: [@umer-78](https://github.com/umer-78)
- Portfolio: [umer-78.github.io](https://umer-78.github.io/)
