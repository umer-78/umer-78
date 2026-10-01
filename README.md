# Umer Hashmi

Software engineer. I build security tools, machine learning and LLM systems,
and applications. Every repository below has a README with real output, a test
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
| [gradient-boosting](https://github.com/umer-78/gradient-boosting) · [demo](https://umer-78.github.io/gradient-boosting/) | Gradient boosting written from scratch: histogram trees, Newton leaf values, early stopping. Every gradient is checked against finite differences, and it shows gain importance ranking a planted noise column above a real predictor while permutation importance scores it zero. |
| [recommender-engine](https://github.com/umer-78/recommender-engine) · [demo](https://umer-78.github.io/recommender-engine/) | Popularity and random baselines, item-item CF, matrix factorisation and BPR on a temporal split. Demonstrates that rating-trained factorisation ranks worse than random, and the same model trained with a pairwise loss ranks 13× better. |
| [anomaly-detection](https://github.com/umer-78/anomaly-detection) · [demo](https://umer-78.github.io/anomaly-detection/) | Statistical detectors and an isolation forest for metrics, with a random detector shipped in the box to show how far point-adjusted F1 flatters a detector — pure noise reaches 0.46 on it, beating the isolation forest's honest 0.42. |
| [image-toolkit](https://github.com/umer-78/image-toolkit) · [demo](https://umer-78.github.io/image-toolkit/) | Image processing from scratch in NumPy: convolution kept distinct from correlation, a separable Gaussian doing 50 multiplies per pixel instead of 625 (14.5× faster in the benchmark) and identical to 1e-13, Otsu thresholding and Canny-style edges. |
| [neural-network-from-scratch](https://github.com/umer-78/neural-network-from-scratch) · [demo](https://umer-78.github.io/neural-network-from-scratch/) | Feed-forward network in pure NumPy. Every hand-derived gradient is checked against a numerical estimate — the test fails if the calculus is wrong. |
| [rag-document-qa](https://github.com/umer-78/rag-document-qa) · [demo](https://umer-78.github.io/rag-document-qa/) | Question answering over your own documents: structure-aware chunking, BM25 + TF-IDF hybrid retrieval, cited answers, no API key. |
| [sentiment-analyzer](https://github.com/umer-78/sentiment-analyzer) · [demo](https://umer-78.github.io/sentiment-analyzer/) | Naive Bayes written from scratch and scored beside scikit-learn's on the same data, with negation handling and per-prediction explanations. |
| [customer-churn-prediction](https://github.com/umer-78/customer-churn-prediction) · [demo](https://umer-78.github.io/customer-churn-prediction/) | Three models and a majority-class baseline compared on one split, with PR-AUC as the headline metric because missing a churner is the costly error, plus a model card and a scoring CLI. |
| [ml-model-serving-api](https://github.com/umer-78/ml-model-serving-api) · [demo](https://umer-78.github.io/ml-model-serving-api/) | FastAPI service for a scikit-learn model: validation, model versioning, rollback, health and metrics endpoints. |

## LLM engineering

| Project | What it does |
| --- | --- |
| [llm-gateway](https://github.com/umer-78/umer-78-llm-gateway) | Self-healing gateway in front of several LLM providers: circuit breakers kept in Redis, failover by request class, hedged requests and a queue that waits out outages, with cost per tenant and feature. Answered 92.2% of interactive requests through scripted outages, against 74.4% when calling one provider directly. |
| [groundtruth](https://github.com/umer-78/groundtruth) · [demo](https://umer-78.github.io/groundtruth/) | Retrieval evaluation for a legal research assistant: 100 questions over 510 real contracts with lawyer-labelled passages. The configuration it recommends finds the passage in the top 10 for 70.0% of questions, against 36.8% for plain BM25, and CI fails any change that costs a point. |
| [doorman](https://github.com/umer-78/doorman) · [demo](https://umer-78.github.io/doorman/) | Prompt-injection defences for an AI recruiting agent, measured against 60 red-team attacks and 303 injections written by others. Isolating what the agent reads from what it may do stopped every one, with no benign application flagged. |
| [warmstart](https://github.com/umer-78/warmstart) · [demo](https://umer-78.github.io/warmstart/) | Semantic cache for an LLM support assistant. Replayed on 10,000 real support questions it answered 29.4% from the cache with 4 wrong answers and no cross-customer leaks, cutting the cost per 1,000 questions from $6.72 to $2.61. |
| [llm-cost-autopilot](https://github.com/umer-78/llm-cost-autopilot) · [demo](https://umer-78.github.io/llm-cost-autopilot/) | Routes each LLM request to the cheapest model likely to get it right. On 4,551 questions with every model's answers recorded by HELM, it matched GPT-4o's accuracy at 23% of the cost. |
| [llm-regression-detector](https://github.com/umer-78/llm-regression-detector) · [demo](https://umer-78.github.io/llm-regression-detector/) | Finds the tasks a model upgrade breaks, with McNemar's test per task and Holm's correction as a CI gate. Llama 3 → 3.1 70B moved 0.7 points overall while legal questions fell from 69.2% to 58.3%. |
| [ai-feature-flags](https://github.com/umer-78/ai-feature-flags) · [demo](https://umer-78.github.io/ai-feature-flags/) | Staged rollouts of a new model or prompt that roll back on their own. It rolled back the three clearly worse upgrades in 100 of 100 replays; with an identical candidate it wrongly rolled back 3.8% of rollouts, against 45.9% for re-running an ordinary test. |
| [prompt-ab-platform](https://github.com/umer-78/prompt-ab-platform) · [demo](https://umer-78.github.io/prompt-ab-platform/) | A/B/n testing for prompts: versioned templates, Thompson sampling and always-valid elimination. On HELM's recorded prompt variants, the prompt format alone moved accuracy by up to 63.8 points. |
| [llm-arbitration](https://github.com/umer-78/llm-arbitration) · [demo](https://umer-78.github.io/llm-arbitration/) | A panel of critics checks each LLM answer, and an adjudicator weighs them by their record into a calibrated verdict. It caught 57% of Llama 3.1 70B's wrong answers where a majority vote caught 43%. |
| [judge-calibration](https://github.com/umer-78/judge-calibration) · [demo](https://umer-78.github.io/judge-calibration/) | GPT-4 as a judge against two pools of human raters on 1,399 outputs. It agrees with each pool about as well as they agree with each other, and favours its own model family by 0.38 points on completeness. |
| [distill](https://github.com/umer-78/distill) · [demo](https://umer-78.github.io/distill/) | Distils GPT-3.5's labels into a model that runs on a CPU: 94.9% against the teacher's 95.3% on held-out reviews, and cheaper to own above 16,865 requests a month. |
| [text-to-sql-guardrails](https://github.com/umer-78/text-to-sql-guardrails) · [demo](https://umer-78.github.io/text-to-sql-guardrails/) | A parsing guard and a database-enforced sandbox between LLM-written SQL and the database. Together they stopped 40 of 40 attacks while all 20 ordinary queries ran, and wrongly blocked none of 322 Spider gold queries. |
| [pipeline-forensics](https://github.com/umer-78/pipeline-forensics) · [demo](https://umer-78.github.io/pipeline-forensics/) | Traces AI pipelines step by step and blames the step a bad answer came from. It shows that Gemini 1.5 Flash 002's 46-point maths "regression" is mostly a stop sequence added between benchmark releases. |
| [self-healing-docs](https://github.com/umer-78/self-healing-docs) · [demo](https://umer-78.github.io/self-healing-docs/) | A GitHub Action that fails pull requests whose API changes leave the docs wrong, and patches renames. Replayed over httpx's history: 33 doc sections went stale, for a median of 52 days. |
| [eval-dataset-generator](https://github.com/umer-78/eval-dataset-generator) · [demo](https://umer-78.github.io/eval-dataset-generator/) | Turns production logs into an evaluation set: redaction, clustering, and sampling that captured 1.7× the failures per labelled case while its quality estimate stayed unbiased. |
| [casefile](https://github.com/umer-78/casefile) · [demo](https://umer-78.github.io/casefile/) | Bounded multi-agent claims triage: typed handoffs, snapshots, cost ceilings enforced in code and a human gate on payouts. Across 900 synthetic claims every run stopped and none crossed its ceiling. |
| [graph-rag](https://github.com/umer-78/graph-rag) · [demo](https://umer-78.github.io/graph-rag/) | Knowledge-graph and vector retrieval over the same chunks, with a router. On hop questions over the top 500 PyPI packages, vector search found 38.3% of what was needed and routed retrieval 99.7%. |
| [research-agents](https://github.com/umer-78/research-agents) · [demo](https://umer-78.github.io/research-agents/) | Multi-agent research with durable state, budgets and cited findings. It answered 94% of sub-questions with 15% of tool calls failing, and every run killed mid-way resumed to the same report. |
| [slotfill](https://github.com/umer-78/slotfill) · [demo](https://umer-78.github.io/slotfill/) | Strict-schema extraction from scanned receipts. A small trained extractor validates 98.5% of the time against 83.5% for rules, gets totals right 94% of the time and runs in under 4 ms on a CPU. |
| [fieldnote](https://github.com/umer-78/fieldnote) · [demo](https://umer-78.github.io/fieldnote/) | Answers read off page images and cited with a crop of where they came from. The right receipt comes first for 87.5% of questions whose answer exists only in the image. |

## Data & analytics

| Project | What it does |
| --- | --- |
| [route-planner](https://github.com/umer-78/route-planner) · [demo](https://umer-78.github.io/route-planner/) | Shortest and fastest routes over a 1,600-intersection network: Dijkstra, A* and bidirectional search sharing one implementation. The heuristic's admissibility is tested against the real network, and a heuristic weighted 1.2 expands *more* nodes than an unweighted one. |
| [text-search](https://github.com/umer-78/text-search) · [demo](https://umer-78.github.io/text-search/) | A search engine built from the index up in pure Python: positions, BM25, phrase and boolean queries, the Porter stemmer and typo tolerance. Uses the clamped idf because the textbook BM25 form measures −1.4351 on a term in 10 of 12 documents, penalising a document for containing the query. |
| [mini-sql-engine](https://github.com/umer-78/mini-sql-engine) · [demo](https://umer-78.github.io/mini-sql-engine/) | A SQL engine written from scratch (tokenizer, recursive-descent parser, executor) running joins, grouping, aggregates, UNION and CASE over CSV files, plus INSERT, UPDATE and DELETE that only reach the files when saved, with three-valued NULL logic and errors that point at the offending character. |
| [timeseries-forecasting](https://github.com/umer-78/timeseries-forecasting) · [demo](https://umer-78.github.io/timeseries-forecasting/) | Baselines, exponential smoothing and rolling-origin backtesting with no dependencies. MASE is scaled by the training window, and a test proves no fold ever sees data past its own origin. |
| [sales-insights](https://github.com/umer-78/sales-insights) · [demo](https://umer-78.github.io/sales-insights/) | pandas analysis with an audit trail: every row dropped in cleaning is counted and explained. Cohort retention, RFM segmentation, seasonality. |
| [ta-indicators](https://github.com/umer-78/ta-indicators) · [demo](https://umer-78.github.io/ta-indicators/) | Dependency-free technical indicators in strict TypeScript, checked against published worked examples. |
| [stocksense](https://github.com/umer-78/stocksense) | Inventory forecasting for Shopify, a replacement for the retired Stocky: days-to-stockout and reorder quantities per variant, with the arithmetic shown behind every number. Remix + Shopify App Bridge, 90 tests over the forecasting, billing and import logic. |

## Applications & services

| Project | What it does |
| --- | --- |
| [leadflow](https://github.com/umer-78/leadflow) | LeadFlow AI: an autonomous lead-intake system for high-value service clinics. A 24/7 AI receptionist bounded by each clinic's verified guidelines (never invents pricing, refuses diagnoses), explainable HIGH/MEDIUM/LOW intent scoring, and follow-up that halts the moment a lead replies or books. Express + Gemini, React/Vite dashboard, multi-tenant. |
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
| [GD_PROJECT](https://github.com/umer-78/GD_PROJECT) · [play](https://umer-78.github.io/GD_PROJECT/play/) | Treasure Hunt, a 3D maze game: five temple levels, sentries whose line of sight is drawn on the floor, telegraphed traps, and a camera that never ends up inside a wall. Built in Unity with C#, and ported to three.js so it plays in the browser. |
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
**LLM systems** ONNX Runtime · sentence embeddings · sqlglot · RapidOCR · Prometheus · Grafana\
**Web** FastAPI · React · Vite · Node · Tailwind CSS · Motion (Framer Motion)\
**Data stores** SQLite · PostgreSQL · Redis\
**Other** Docker · GitHub Actions · Unity · pytest · xUnit · Vitest\
**AI tooling** 21st.dev MCP · UI UX Pro Max

## Reach me

- GitHub: [@umer-78](https://github.com/umer-78)
- Portfolio: [umer-78.github.io](https://umer-78.github.io/)
