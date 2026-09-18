# Umer Hashmi

Software engineer. I build security tooling, machine learning projects and
applications — and I finish them: every repository below has a README with real
output, a test suite, and CI that builds it on a clean machine.

**Portfolio: [umer-78.github.io](https://umer-78.github.io/)**

---

## Security & networking

| Project | What it does |
| --- | --- |
| [password-strength-checker](https://github.com/umer-78/password-strength-checker) | Offline password analyzer — entropy, leetspeak, keyboard walks, dates, passphrase scoring, and a `--min-score` CLI gate. |
| [log-sentinel](https://github.com/umer-78/log-sentinel) | Finds SSH brute-force, password spraying and success-after-failure logins in Linux auth logs. |
| [file-integrity-monitor](https://github.com/umer-78/file-integrity-monitor) | SHA-256 baselines with HMAC signing, so a tampered *baseline* is caught too. Watch mode included. |
| [security-headers-scanner](https://github.com/umer-78/security-headers-scanner) | Grades a site's HTTP security headers and cookies A–F, with the exact header line that fixes each finding. |
| [subnet-calculator](https://github.com/umer-78/subnet-calculator) · [demo](https://umer-78.github.io/subnet-calculator/) | IPv4 subnetting, equal split and VLSM in the browser. The maths module has no DOM in it, so it is unit tested. |

## Machine learning & AI

| Project | What it does |
| --- | --- |
| [gradient-boosting](https://github.com/umer-78/gradient-boosting) | Gradient boosting written from scratch — histogram trees, Newton leaf values, early stopping. Every gradient is checked against finite differences, and it shows gain importance ranking a planted noise column above a real predictor while permutation importance scores it zero. |
| [recommender-engine](https://github.com/umer-78/recommender-engine) | Popularity and random baselines, item-item CF, matrix factorisation and BPR on a temporal split. Demonstrates that rating-trained factorisation ranks worse than random, and the same model on a pairwise loss is 13× better. |
| [anomaly-detection](https://github.com/umer-78/anomaly-detection) | Statistical detectors and an isolation forest for metrics, with a random detector shipped in the box to show how far point-adjusted F1 flatters a detector — pure noise scores 0.46 on it against a real 0.08. |
| [image-toolkit](https://github.com/umer-78/image-toolkit) | Image processing from scratch in NumPy: convolution kept distinct from correlation, a separable Gaussian 11× faster and identical to 1e-13, Otsu thresholding and Canny-style edges. |
| [neural-network-from-scratch](https://github.com/umer-78/neural-network-from-scratch) | Feed-forward network in pure NumPy. Every hand-derived gradient is checked against a numerical estimate — the test fails if the calculus is wrong. |
| [rag-document-qa](https://github.com/umer-78/rag-document-qa) | Question answering over your own documents: structure-aware chunking, BM25 + TF-IDF hybrid retrieval, cited answers, no API key. |
| [sentiment-analyzer](https://github.com/umer-78/sentiment-analyzer) | Naive Bayes written from scratch and scored beside scikit-learn's on the same data, with negation handling and per-prediction explanations. |
| [customer-churn-prediction](https://github.com/umer-78/customer-churn-prediction) | Four models compared honestly against a baseline, with the decision threshold chosen from the cost of a false negative rather than from accuracy. |
| [ml-model-serving-api](https://github.com/umer-78/ml-model-serving-api) | FastAPI service for a scikit-learn model: validation, model versioning, rollback, health and metrics endpoints. |

## Data & analytics

| Project | What it does |
| --- | --- |
| [mini-sql-engine](https://github.com/umer-78/mini-sql-engine) | A SQL engine written from scratch — tokenizer, recursive-descent parser and executor — running joins, grouping and aggregates over CSV files, with three-valued NULL logic and errors that point at the offending character. |
| [timeseries-forecasting](https://github.com/umer-78/timeseries-forecasting) | Baselines, exponential smoothing and rolling-origin backtesting with no dependencies. MASE is scaled by the training window, and a test proves no fold ever sees data past its own origin. |
| [sales-insights](https://github.com/umer-78/sales-insights) | pandas analysis with an audit trail — every row dropped in cleaning is counted and explained. Cohort retention, RFM segmentation, seasonality. |
| [ta-indicators](https://github.com/umer-78/ta-indicators) | Dependency-free technical indicators in strict TypeScript, checked against published worked examples. |

## Applications & services

| Project | What it does |
| --- | --- |
| [bank-ledger-csharp](https://github.com/umer-78/bank-ledger-csharp) | Append-only account ledger in C#/.NET 8. Money is `decimal`, entries are never edited, and `audit` replays every entry to prove the balance still agrees. |
| [kv-store](https://github.com/umer-78/kv-store) | A log-structured key-value store in Go — write-ahead log, SSTables, bloom filters and compaction. Reading an absent key is 50× faster than a present one, and a crash mid-write loses only what was never acknowledged. |
| [loadgun](https://github.com/umer-78/loadgun) | HTTP load testing in Go — worker pool, rate cap, nearest-rank percentiles and a latency histogram, exiting non-zero so it works as a CI gate. |
| [url-shortener-go](https://github.com/umer-78/url-shortener-go) | URL shortener in Go: JSON API, custom codes, expiring links, atomic visit counting, single static binary, distroless image. |
| [inventory-management-system](https://github.com/umer-78/inventory-management-system) | Stock control on a movement-ledger design — stock on hand is derived, never a field that can drift. Suppliers, purchase orders, valuation, reorder alerts. |
| [project-tracker](https://github.com/umer-78/project-tracker) | Team project management: kanban with drag and drop, sprints, burndown, workload and role-based permissions. |
| [task-board](https://github.com/umer-78/task-board) · [demo](https://umer-78.github.io/task-board/) | Kanban in React and TypeScript where every drag has a keyboard equivalent. |
| [weather-now](https://github.com/umer-78/weather-now) · [demo](https://umer-78.github.io/weather-now/) | Weather dashboard on the keyless Open-Meteo API. The hourly strip starts at the current hour, not at midnight. |
| [coinvantage](https://github.com/umer-78/coinvantage) · [demo](https://umer-78.github.io/coinvantage/) | Installable crypto markets site — live prices, charts, signals and an on-device forecast. No API keys, no trading, no wallet access. |

## Games & interactive

| Project | What it does |
| --- | --- |
| [GD_PROJECT](https://github.com/umer-78/GD_PROJECT) | Unity 3D maze game: recursive-backtracker levels carved at runtime, enemies that check line of sight before firing, collectibles and traps. |
| [snake-game](https://github.com/umer-78/snake-game) · [demo](https://umer-78.github.io/snake-game/) | Snake on a canvas with the rules separated from the rendering and unit tested — queued turns mean two fast key presses can't fold the snake into itself. |

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

**Languages** Python · JavaScript · TypeScript · C# · Go · SQL
**ML & data** NumPy · pandas · scikit-learn · Matplotlib
**Web** FastAPI · React · Vite · Node
**Data stores** SQLite · PostgreSQL
**Other** Docker · GitHub Actions · Unity · pytest · xUnit · Vitest

## Reach me

- GitHub: [@umer-78](https://github.com/umer-78)
- Portfolio: [umer-78.github.io](https://umer-78.github.io/)
