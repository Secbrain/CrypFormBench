# CrypFormBench (C.F.B) · Benchmarking LLMs for Formal Analysis of Cryptographic Schemes

<p align="center">
  <img src="overview.png" alt="Overview of CrypFormBench" width="78%">
</p>

<p align="center">
  <a href="#-quick-links"><img src="https://img.shields.io/badge/Docs-Quick%20Start-blue"></a>
  <a href="#-results--figures"><img src="https://img.shields.io/badge/Figures-Auto--Generated-success"></a>
  <a href="#-license"><img src="https://img.shields.io/badge/License-Open%20Source-lightgrey"></a>
  <a href="#-citing"><img src="https://img.shields.io/badge/Cite-This%20Work-important"></a>
</p>

> **Goal:** A reproducible benchmark + toolkit to evaluate LLMs on **interpreting, generating, completing, converting, and fixing** formal specifications of cryptographic schemes and protocols across multiple verification frameworks.

---

## View web page on https://Secbrain.github.io/CrypFormBench

## 🔗 Quick Links

- **[Leaderboard Snapshot]()** · **[Datasets]()** · **[Quick Start]()** · **[Reproduce the Benchmark]()** · **[Evaluate a New Model]()**
- **[Repository Layout]()** · **[Data Formats]()** · **[Results & Figures]()**
- **[References]()** · **[FAQ]()**

---

## 🏆 Overall Leaderboard (recomputed by §4.5)

> **S_overall (recalc)** uses §4.5: executable tasks use \(S_\text{task}=\mathrm{HM}(a,\mathrm{HM}(\mathrm{ACC}_A,\mathrm{F1}_A))\);  
> interpretation uses \(\alpha s_\text{logic}+\beta s_\text{anno}+(1-\alpha-\beta)\mathrm{HM}(a,\mathrm{HM}(\mathrm{ACC}_A,\mathrm{F1}_A))\) with \(\alpha=\beta=0.3\).  
> Overall weights: gen 0.25, comp 0.20, trans 0.25, corr 0.15, interp 0.15.

<!-- LEADERBOARD_OVERALL:BEGIN -->

<table>
  <thead>
    <tr>
      <th align="right">Rank</th>
      <th align="left">Model</th>
      <th align="center">S_overall (recalc)</th>
      <th align="left">Progress</th>
      <th align="left">Badge</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="right">🥇 1</td>
      <td><b>Claude-3.5-Sonnet-Coder</b></td>
      <td align="center"><b>48.7</b></td>
      <td>██████████░░░░░░░░░ (49%)</td>
      <td><img src="https://img.shields.io/badge/Overall-51.0-2ea44f?labelColor=111" alt="51.0"></td>
    </tr>
    <tr>
      <td align="right">🥈 2</td>
      <td><b>DeepSeek-Coder</b></td>
      <td align="center"><b>38.6</b></td>
      <td>████████░░░░░░░░░░░ (39%)</td>
      <td><img src="https://img.shields.io/badge/Overall-38.6-3fb950?labelColor=111" alt="38.6"></td>
    </tr>
    <tr>
      <td align="right">🥉 3</td>
      <td><b>GPT-4o</b></td>
      <td align="center"><b>35.0</b></td>
      <td>███████░░░░░░░░░░░░ (35%)</td>
      <td><img src="https://img.shields.io/badge/Overall-35.0-4caf50?labelColor=111" alt="35.0"></td>
    </tr>
    <tr>
      <td align="right">4</td>
      <td>DeepSeek-R1</td>
      <td align="center">34.6</td>
      <td>███████░░░░░░░░░░░░ (35%)</td>
      <td><img src="https://img.shields.io/badge/Overall-34.6-74c69d?labelColor=111" alt="34.6"></td>
    </tr>
    <tr>
      <td align="right">5</td>
      <td>LLaMA4-Instruct</td>
      <td align="center">27.8</td>
      <td>█████░░░░░░░░░░░░░ (28%)</td>
      <td><img src="https://img.shields.io/badge/Overall-27.8-a3b1c2?labelColor=111" alt="27.8"></td>
    </tr>
    <tr>
      <td align="right">6</td>
      <td>GPT-4o-mini</td>
      <td align="center">23.0</td>
      <td>█████░░░░░░░░░░░░░ (23%)</td>
      <td><img src="https://img.shields.io/badge/Overall-23.0-8b949e?labelColor=111" alt="23.0"></td>
    </tr>
    <tr>
      <td align="right">7</td>
      <td>Gemini-2.5-Pro</td>
      <td align="center">22.8</td>
      <td>█████░░░░░░░░░░░░░ (23%)</td>
      <td><img src="https://img.shields.io/badge/Overall-22.8-8b949e?labelColor=111" alt="22.8"></td>
    </tr>
    <tr>
      <td align="right">8</td>
      <td>Grok-3</td>
      <td align="center">18.0</td>
      <td>███░░░░░░░░░░░░░░░ (18%)</td>
      <td><img src="https://img.shields.io/badge/Overall-18.0-8b949e?labelColor=111" alt="18.0"></td>
    </tr>
    <tr>
      <td align="right">9</td>
      <td>GLM-4</td>
      <td align="center">16.1</td>
      <td>███░░░░░░░░░░░░░░░ (16%)</td>
      <td><img src="https://img.shields.io/badge/Overall-16.1-8b949e?labelColor=111" alt="16.1"></td>
    </tr>
  </tbody>
</table>
<!-- LEADERBOARD_OVERALL:END -->

---

## 🧭 Capability Leaderboards (recomputed)

> Executable tasks: \(S_\text{task}=\mathrm{HM}(a,\mathrm{HM}(\mathrm{ACC}_A,\mathrm{F1}_A))\).  
> Interpretation uses similarity-weighted formula (\(\alpha=\beta=0.3\)). Scores in [0,100].

### 📝 Interpret
<!-- LEADERBOARD_INTERPRET:BEGIN -->

| Rank | Model                     | S_interpret (recalc) |
|:-----:|---------------------------|:--------------------:|
| 🥇 1 | GPT-4o                    | **94.1**             |
| 🥈 2 | GPT-4o-mini               | 93.8                 |
| 🥉 3 | DeepSeek-Coder            | 93.2                 |
| 4    | Claude-3.5-Sonnet-Coder   | 91.7                 |
| 5    | DeepSeek-R1               | 77.4                 |
| 6    | Gemini-2.5-Pro            | 69.1                 |
| 7    | GLM-4                     | 62.3                 |
| 8    | Grok-3                    | 49.6                 |
| 9    | LLaMA4-Instruct           | 44.4                 |

<!-- LEADERBOARD_INTERPRET:END -->

### 🧱 Generation
<!-- LEADERBOARD_GENERATE:BEGIN -->
| Rank | Model                     | S_generate (recalc) |
|:----:|---------------------------|:-------------------:|
| 🥇 1 | Claude-3.5-Sonnet-Coder   | **24.2**            |
| 🥈 2 | Grok-3                    | 12.8                |
| 🥉 3 | GPT-4o                    | 9.5                 |
| 4    | Gemini-2.5-Pro            | 7.7                 |
| 5    | DeepSeek-Coder            | 5.8                 |
| 6    | DeepSeek-R1               | 5.8                 |
| 7    | LLaMA4-Instruct           | 5.8                 |
| 8    | GLM-4                     | 0.0                 |
| 9    | GPT-4o-mini               | 0.0                 |

<!-- LEADERBOARD_GENERATE:END -->

### 🧩 Completion
<!-- LEADERBOARD_COMPLETE:BEGIN -->
| Rank | Model                     | S_complete (recalc) |
|:----:|---------------------------|:-------------------:|
| 🥇 1 | Claude-3.5-Sonnet-Coder   | **74.4**            |
| 🥈 2 | DeepSeek-Coder            | 68.0                |
| 🥉 3 | DeepSeek-R1               | 65.2                |
| 4    | LLaMA4-Instruct           | 55.6                |
| 5    | GPT-4o                    | 51.5                |
| 6    | Grok-3                    | 36.7                |
| 7    | Gemini-2.5-Pro            | 25.9                |
| 8    | GLM-4                     | 22.8                |
| 9    | GPT-4o-mini               | 10.9                |

<!-- LEADERBOARD_COMPLETE:END -->

### 🛠 Correction
<!-- LEADERBOARD_FIX:BEGIN -->
| Rank | Model                     | S_fix (recalc) |
|:----:|---------------------------|:--------------:|
| 🥇 1 | Claude-3.5-Sonnet-Coder   | **71.2**       |
| 🥈 2 | DeepSeek-Coder            | 63.9           |
| 🥉 3 | LLaMA4-Instruct           | 57.2           |
| 4    | DeepSeek-R1               | 56.9           |
| 5    | GPT-4o                    | 54.7           |
| 6    | GPT-4o-mini               | 44.8           |
| 7    | Gemini-2.5-Pro            | 35.6           |
| 8    | GLM-4                     | 14.5           |
| 9    | Grok-3                    | 0.0            |

<!-- LEADERBOARD_FIX:END -->

### 🔁 Transformation
<!-- LEADERBOARD_CONVERT:BEGIN -->
| Rank | Model                     | S_convert (recalc) |
|:----:|---------------------------|:------------------:|
| 🥇 1 | Claude-3.5-Sonnet-Coder   | **13.3**           |
| 2–9  | Others                    | 0.0                |

<!-- LEADERBOARD_CONVERT:END -->

---

## 🗂️ Datasets

Our dataset is curated to reflect the **full lifecycle of cryptographic protocols/schemes**—from *design-time intent* to *implementation-level artifacts*—and to exercise models across **multiple formal languages**, **attacker models**, and **security properties**.

<div align="center">
  <img src="datasets/protocols.png" alt="Word cloud of schemes/protocols" width="48%">
  <img src="datasets/propeties.png" alt="Word cloud of verified propeties" width="48%">
  <br>
  <sub><b>Left:</b> Word cloud of schemes/protocols. · <b>Right:</b> Word cloud of verified properties.</sub>
</div>


> In short: **design** covers what the scheme is intended to guarantee (symbolic & computational properties), while **implementation** highlights what the low-level crypto code is checked for with <i>Jasmin</i>, aligning the model’s reasoning from specs to realizations.

### What it covers

- **Stages (design → implementation)**
  - **Design security (scheme-level)**: natural-language specs, goal statements, role/I/O and trust assumptions (e.g., secrecy, authentication, integrity, freshness, forward secrecy, equivalence, IND-)
  - **Structured designs**: message-sequence charts, role tables, state machines
  - **Implementation security (Jasmin-level)**: artifacts and checks around low-level crypto code in **Jasmin**, focusing on side-channel discipline (e.g., constant-time style) and verifier-guided sanity checks that complement the formal specs.
- **Tasks & capabilities**
  - **Interpret** (explain/annotate formal code)
  - **Generation** (from scratch, guided by goals/assumptions)
  - **Completion** (fill missing blocks in valid specs)
  - **Transformation** (cross-language translation with semantics preserved)
  - **Correction** (syntax- and semantics-guided repair using verifier feedback)
- **Security properties (symbolic & computational)**
  - **Secrecy/confidentiality**, **authentication** (entity, mutual, injective/non-injective), **integrity**
  - **Freshness**, **replay resistance**, **session binding**, **channel binding**
  - **Forward secrecy / PFS**, **KCI/AKC resistance**, **key compromise resilience**
  - **Unlinkability/anon/pseudonymity**, **agreement** (aliveness/weak/strong), **resistance to MitM**
  - **IND-CPA/IND-CCA families** (in computational settings), **equivalence** properties (trace/bihyper)
- **Attacker models**
  - **Dolev–Yao** network adversary, **state reveal/ephemeral key leak**, **CK/eCK**-style models
  - Tool-specific backends and semantics (e.g., ProVerif queries, Tamarin lemmas, AVISPA backends, Maude-NPA equational theories, CryptoVerif/EasyCrypt reductions)
- **Languages & tools**
  - **ProVerif**, **Tamarin**, **Scyther**, **Maude-NPA**, **AVISPA**, **CryptoVerif**, **EasyCrypt**
  - Each instance includes *tool config, timeouts, flags*, and expected verdict normalization

---

## 📋 Prompt & Example Evaluation Trace

This benchmark ships examples of *evaluation traces* for each task under `html/*.json`.
**Important:** the structure of the JSON is discovered dynamically by unwrapping to the “language → model → record” layer.

### JSON Structure (schema, root-agnostic)

```json
{
  "<any-root-key>": {
    "<language>": {
      "<model>": {
        "filename": "string",
        "inputdata": { /* dataset content object or string */ },
        "prompt": [ /* chat-style messages OR a string */ ],
        "modelinput": [ /* the exact model input after templating */ ],
        "model": "string",             /* (optional) model name */
        "modeloutput": "string|object",
        "evalresult": { /* metrics / bookkeeping */ }
      }
    }
  }
}
````


### 🔁 Five-stage pipeline

1. **Dataset content (`inputdata`)**
2. **Prompt (`prompt`)**
3. **Model input (`modelinput`)** – after templating/assembly
4. **Model output (`modeloutput`)**
5. **Eval result (`evalresult`)**

Each stage is logged per *(task, language, model)*.


### 💡 Example (from `html/generation.json`)

**Task**: `generation`
**Language**: `ec`
**Model**: `llama4-maverick-instruct-basic`
**Filename**: `EC-1/KEMDEM.ec`

<b>① Dataset Content (inputdata)</b> — expand to view</summary>

```json
{
  "file": "EC-1/KEMDEM.ec",
  "logic": "… full logic/program text …",
  "results": { "…": "…" }
}
```

<b>② Prompt (prompt)</b> — chat-style template

```json
[
  {
    "role": "system",
    "content": "You are an expert on formal verification for cryptographic schemes, specialized in the <tool_name> tool. I will give you a logic description file ..."
  },
  {
    "role": "user",
    "content": "… instruction + dataset excerpt …"
  }
]
```

<b>③ Model Input (modelinput)</b> — the exact payload sent to the model

```json
[
  { "role": "system", "content": "You are an expert … EasyCrypt tool. I will give you a logic description file …" },
  { "role": "user", "content": "… fully constructed user message with embedded logic …" }
]
```

<b>④ Model Output (modeloutput)</b> — model’s response

```text
Based on the given description of the KEM-DEM construction …
… (full generated code / explanation here) …
```

<b>⑤ Eval Result (evalresult)</b> — scoring & bookkeeping

```json
{
  "num_generates": 1,
  "num_analysis": 0,
  "num_timeout": 0,
  "tp": 0, "tn": 0, "fp": 0, "fn": 0,
  "timeuse": null,
  "filesize": 0,
  "score": "… task-specific metric …"
}
```

> Tip: On the website https://Secbrain.github.io/CrypFormBench, the "Evaluation Process" panel defaults to
> `generation / <available-language> / llama4-maverick-instruct-basic`.
> You can switch task/language/model from the dropdowns; the five blocks above are populated from the
> corresponding JSON entry.


### 🔗 Where the cases lives

* Web UI loads from: `html/generation.json`, `html/completion.json`, `html/translation.json`,
  `html/interpretation_logic.json`, `html/interpretation_notation.json`,
  `html/correction_false.json`, `html/correction_error.json`.
* Each file follows the schema above (root key can vary). The site auto-detects the language layer.

---

## 🚀 Quick Start

> **Requirements:** Python 3.10+ and `pip`. External verifiers are optional if you only run aggregation/plotting on provided logs.

```bash
# 1) Clone
git clone https://github.com/Secbrain/CrypFormBench.git
cd CrypFormBench

# 2) (Optional) Virtual env
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate

# 3) Install
pip install -r code/requirements.txt

# 4) Sanity checks
python -m code.tools.check_repo

# 5) Rebuild metrics from existing outputs + logs
python -m code.metrics.aggregate \
  --model-outputs model_outputs \
  --original-results original_results \
  --out calculated_results

# 6) Generate all figures
python -m code.viz.plot_all \
  --in calculated_results \
  --out result_figures
```

> 💡 No verifier installed? You can still reproduce tables/plots from `original_results/`.

---

## 🧪 Reproducing the Benchmark

**Pipeline:** *generate → verify → score → visualize*

1. **Generate model outputs**

```bash
python -m code.run.generate \
  --model gpt-4o \
  --tasks datasets/tasks.yaml \
  --prompts datasets/prompts \
  --out model_outputs/gpt-4o
```

2. **Verify with external tools** (ProVerif, Tamarin, Scyther, Maude-NPA, AVISPA, CryptoVerif, EasyCrypt…)

```bash
python -m code.run.verify \
  --inputs model_outputs/gpt-4o \
  --tool-config code/tools/tools.yaml \
  --out original_results/gpt-4o
```

3. **Score & aggregate**

```bash
python -m code.metrics.aggregate \
  --model-outputs model_outputs/gpt-4o \
  --original-results original_results/gpt-4o \
  --out calculated_results/gpt-4o
```

4. **Visualize**

```bash
python -m code.viz.plot_all \
  --in calculated_results \
  --out result_figures
```

---

## 📦 Repository Layout

```
├─ calculated_results/   # Derived metrics & summary tables (per model / per task)
├─ code/                 # Runners, scorers, plotting, tool adapters, sanity checks
│  ├─ run/               # generate.py, verify.py
│  ├─ metrics/           # aggregate.py, scoring utilities
│  ├─ viz/               # plot_all.py, figure helpers
│  └─ tools/             # external tool wrappers, configs, schema checks
├─ datasets/             # Capability descriptions, tasks, prompts, schemas
│  ├─ prompts/           # Prompt templates per task/language
│  └─ README.md          # Dataset documentation & taxonomy
├─ model_outputs/        # Raw generations (model × task)
├─ original_results/     # Verifier logs / normalized verdicts
├─ result_figures/       # Publication-ready plots (PNG/SVG/PDF)
└─ overview.png          # High-level pipeline diagram
└─ index.html            # View of HTML File
└─ html                  # Process of evaluation cases and vedios
```

---

## 🧰 Data Formats & Conventions

**Task spec (`datasets/`)**

* `id`, `language` (proverif, tamarin, scyther, avv, maude-npa, cryptoverif, easycrypt)
* `capability` (interpret | generate | complete | convert | fix)
* `properties` (goals, attacker model, equivalence/reachability, etc.)
* `inputs` (prompts, partial specs, seeds)
* `evaluation` (tool, flags, timeouts)

**Model outputs (`model_outputs/<model>/<task_id>.*`)**

* The exact artifact for the tool (e.g., `.pv`, `.spthy`, `.if`, `.maude`, `.ocv`, `.ec`)
* Sidecar JSON: generation params, prompt hash, timestamp

**Verification logs (`original_results/<model>/<task_id>.log` + `…verdict.json`)**

* Raw stdout/stderr
* Normalized verdict:

```json
  {"analyzable": true, "status": "safe|attack|unknown|error",
   "time_sec": 3.21, "tool_version": "x.y.z"}
```

**Calculated results (`calculated_results/`)**

* Per-task: analyzability `a`, accuracy on analyzable set `ACC_A`, `F1_A`, runtime stats
* Aggregates: by capability, by language, and overall scores

---

## 📊 Results & Figures

All figures in **`result_figures/`** are generated from **`calculated_results/`**.

Common plots:

* Capability comparison (interpret/generate/complete/convert/fix)
* Per-language breakdown
* Analyzability vs. correctness scatter
* Runtime distributions & failure taxonomy (if available)

Rebuild:

```bash
python -m code.viz.plot_all --in calculated_results --out result_figures
```

---

## ➕ Evaluate a New Model

```bash
# 1) Add your model (API or local) in your config
# 2) Generate
python -m code.run.generate \
  --model <your-model> \
  --tasks datasets/tasks.yaml \
  --prompts datasets/prompts \
  --out model_outputs/<your-model>

# 3) (Optional) Verify to produce original_results/<your-model>/
python -m code.run.verify \
  --inputs model_outputs/<your-model> \
  --tool-config code/tools/tools.yaml \
  --out original_results/<your-model>

# 4) Aggregate & plot
python -m code.metrics.aggregate \
  --model-outputs model_outputs/<your-model> \
  --original-results original_results/<your-model> \
  --out calculated_results/<your-model>
python -m code.viz.plot_all \
  --in calculated_results/<your-model> \
  --out result_figures
```

---

## 🧩 Extend with a New Task / Language

* Add a task spec under `datasets/` and its prompt(s) under `datasets/prompts/`.
* New backend? Implement a wrapper in `code/tools/` exposing:

  * `prepare(inputs) -> artifact_path`
  * `run(artifact_path, timeout, flags) -> (raw_log, normalized_verdict_json)`
* Register the task in `datasets/tasks.yaml`.
* (Optional) Update plotting to include the new language/capability.

---

## ❓ FAQ

**Do I need every verifier installed?**
No. Use `original_results/` to run scoring/plotting without local tools.

**What metrics do you report?**
Analyzability `a`, `ACC_A`, `F1_A` on the analyzable subset, plus capability-, language-, and overall aggregates. Runtime/error breakdowns when available.

**Are prompts fixed?**
Yes—prompt templates and inputs in `datasets/` ensure exact replication. Add a new prompt set with a new ID if you want variants.

---

## 📜 License

Add your license here (e.g., MIT). If any dataset includes third-party material, ensure redistribution is permitted and credit original sources.

---

> **Reproducibility first.** From raw model outputs to final plots, everything is scripted and deterministic—so others can re-run your exact pipeline with a few commands.

## 📚 References

- **ProVerif** — Bruno Blanchet. *Automatic Verification of Security Protocols with Secrecy and Authentication.* (Foundational docs and subsequent manuals).
- **Tamarin Prover** — Benedikt Schmidt, Santiago G. Álvarez, David Basin et al. *Automated Verification of Security Protocols with Tamarin.*
- **Scyther** — Cas Cremers. *Scyther: Semantics and Verification of Security Protocols.*
- **AVISPA** — Alessandro Armando et al. *The AVISPA Tool for the Automated Validation of Internet Security Protocols and Applications.*
- **Maude-NPA** — Santiago Escobar, Catherine Meadows, José Meseguer et al. *Maude-NPA: Cryptographic Protocol Analysis Modulo Equational Properties.*
- **CryptoVerif** — Bruno Blanchet. *A Computationally Sound Mechanized Prover for Security Protocols.*
- **EasyCrypt** — Gilles Barthe, Benjamin Grégoire, Sylvain Heraud, Santiago Zanella-Béguelin et al. *Computer-Aided Security Proofs for Cryptographic Programs.*
- **Symbolic vs. Computational** — Ran Canetti; Shoup; Bellare & Rogaway. Canonical works on UC, IND-CPA/CCA, and reductionist proofs.
- **Program Repair/Tool-in-the-Loop** — Works on syntax- and feedback-guided repair that inspire our “fix” tasks and verifier-feedback loops.
