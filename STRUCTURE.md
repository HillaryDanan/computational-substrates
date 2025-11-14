# Repository Structure

**Last Updated:** November 14, 2025

This document explains the organization of the `computational-substrates` repository and the rationale behind each component.

---

## 📁 Current Structure (Phase 1)

```
computational-substrates/
├── README.md                          # Main entry point (you are here!)
├── STRUCTURE.md                       # This document
├── CONTRIBUTING.md                    # Contribution guidelines
├── LICENSE                            # CC BY 4.0
│
├── paper/
│   ├── computational_substrates.md    # Main paper (~40,000 words)
│   ├── abstract.md                    # Standalone abstract
│   ├── executive_summary.md           # 2-page summary for busy readers
│   └── supplementary/
│       ├── mathematical_proofs.md     # Formal derivations
│       ├── extended_examples.md       # Additional case studies
│       └── historical_context.md      # Development of key ideas
│
├── figures/                           # Visual explanations
│   ├── conceptual/
│   │   ├── substrate_comparison.svg   # Silicon vs biology overview
│   │   ├── von_neumann_bottleneck.svg # Memory-processing separation
│   │   ├── energy_time_tradeoff.svg   # Speed vs efficiency plot
│   │   └── hybrid_architecture.svg    # Combined substrate systems
│   ├── data/
│   │   └── (empirical results as they become available)
│   └── README.md                      # Figure descriptions and sources
│
├── predictions/
│   ├── README.md                      # Overview of all predictions
│   ├── 01_substrate_task_matching/
│   │   ├── protocol.md                # Detailed experimental protocol
│   │   ├── rationale.md               # Why this prediction matters
│   │   └── code/                      # Simulation/analysis code
│   ├── 02_energy_scaling_laws/
│   │   ├── protocol.md
│   │   ├── rationale.md
│   │   └── code/
│   ├── 03_cognitive_ability_distribution/
│   ├── 04_neuromorphic_crossover/
│   ├── 05_hybrid_superiority/
│   ├── 06_graceful_degradation/
│   └── 07_algorithm_optimality/
│
├── experiments/                       # Empirical validation
│   ├── README.md                      # Overview of experimental work
│   └── (experiments added as conducted)
│
├── docs/                              # Accessible documentation
│   ├── glossary.md                    # Technical terms explained
│   ├── FAQs.md                        # Common questions
│   ├── key_insights.md                # Non-technical summary
│   ├── practical_implications.md      # For practitioners
│   ├── case_studies_summary.md        # Condensed case studies
│   └── further_reading.md             # Related resources
│
├── references/
│   ├── bibliography.bib               # All 169+ citations
│   ├── key_papers/
│   │   ├── README.md                  # Annotated reading list
│   │   └── (links to papers, organized by topic)
│   └── tools.md                       # Software/hardware for testing
│
└── assets/
    ├── citation.bib                   # BibTeX for citing this work
    └── logos/                         # Branding (if needed)
```

---

## 🎯 Design Principles

### 1. **Separation of Stable vs. Evolving**

**Stable** (unlikely to change significantly):
- `paper/` - Core theoretical framework
- `docs/` - Conceptual explanations
- `references/` - Literature base

**Evolving** (grows over time):
- `predictions/` - Adds protocols, then results
- `experiments/` - Adds new empirical work
- `figures/` - Adds visualizations as created

### 2. **Accessibility Gradient**

Readers can enter at appropriate level:
- **General audience** → `docs/key_insights.md`, `docs/glossary.md`
- **Practitioners** → `docs/practical_implications.md`, `README.md`
- **Researchers** → `paper/computational_substrates.md`, `predictions/`
- **Contributors** → `CONTRIBUTING.md`, specific `protocol.md` files

### 3. **Self-Contained Predictions**

Each prediction folder is **independent and complete**:
- `protocol.md` - Step-by-step experimental design
- `rationale.md` - Why this prediction matters
- `code/` - Simulation and analysis tools
- `results/` - Empirical findings (when available)

Anyone can pick ONE prediction, understand it fully, and test it independently.

### 4. **Reproducibility First**

All empirical work includes:
- Detailed protocols
- Analysis code
- Raw data (when shareable)
- Statistical methods
- Confidence intervals

**Principle:** If someone can't reproduce it, we haven't communicated well enough.

---

## 📈 Evolution Plan

### Phase 1: Foundation (Current - December 2025)

**Goal:** Establish core framework and make it accessible.

**Deliverables:**
- ✅ Core paper
- ✅ README and structure
- ⏳ Conceptual figures
- ⏳ Detailed prediction protocols
- ⏳ Accessible documentation

**Files to create:**
```
figures/conceptual/*.svg        (4 key diagrams)
predictions/*/protocol.md       (7 protocols)
predictions/*/rationale.md      (7 rationales)
docs/*.md                       (6 accessibility documents)
```

### Phase 2: Validation Preparation (January 2026)

**Goal:** Enable others to test predictions.

**Deliverables:**
- Code for simulations (Predictions #1, #2)
- Detailed statistical analysis plans
- Pre-registration of hypotheses
- Community outreach (share on relevant forums)

**Files to create:**
```
predictions/01_substrate_task_matching/code/
    ├── simulate_tasks.py
    ├── compute_match_scores.py
    ├── statistical_analysis.R
    └── README.md

predictions/02_energy_scaling_laws/code/
    ├── measure_silicon_energy.py
    ├── measure_neuromorphic_energy.py
    ├── compare_scaling.py
    └── README.md
```

### Phase 3: Empirical Testing (Q1-Q2 2026)

**Goal:** Test at least 2 predictions empirically.

**Deliverables:**
- Empirical data for Prediction #2 (energy scaling)
- Empirical data for Prediction #1 (substrate-task matching)
- Analysis and writeup of results

**Files to create:**
```
experiments/energy_scaling/
    ├── README.md               (Overview)
    ├── methodology.md          (How we measured)
    ├── data/                   (Raw measurements)
    ├── analysis/               (Statistical analysis)
    └── results.md              (Findings and interpretation)

experiments/substrate_task_matching/
    ├── README.md
    ├── tasks/                  (Task definitions)
    ├── data/
    ├── analysis/
    └── results.md
```

### Phase 4: Iteration and Extension (Q3-Q4 2026)

**Goal:** Refine framework based on empirical results, extend to new domains.

**Possible additions:**
```
paper/revisions/
    ├── v1.1_summary_of_changes.md
    └── updated_computational_substrates.md

extensions/
    ├── quantum_computing/
    │   ├── framework_application.md
    │   └── predictions.md
    ├── optical_computing/
    └── dna_computing/

applications/
    ├── neuromorphic_design_guidelines/
    ├── hybrid_architecture_patterns/
    └── cognitive_augmentation_principles/
```

---

## 🗂️ File Naming Conventions

### General Rules
- Use `snake_case` for filenames: `my_document.md`
- Use descriptive names: `energy_scaling_protocol.md` not `protocol2.md`
- Number prediction folders: `01_substrate_task_matching/`
- Date experimental results: `results_2026_03_15.csv`

### Special Files
- `README.md` - Overview/index for each directory
- `protocol.md` - Experimental protocol (in predictions/)
- `rationale.md` - Motivation and importance (in predictions/)
- `results.md` - Findings from experiments

### Code
- Python scripts: `descriptive_name.py`
- Jupyter notebooks: `01_exploration.ipynb`, `02_analysis.ipynb`
- R scripts: `statistical_analysis.R`
- Always include `requirements.txt` or `environment.yml`

---

## 🤝 Contributing to Structure

### Adding New Content

**New prediction?**
1. Create folder: `predictions/08_new_prediction_name/`
2. Add: `protocol.md`, `rationale.md`, `README.md`
3. Update `predictions/README.md` to list it

**New experiment?**
1. Create folder: `experiments/experiment_name/`
2. Add: `README.md`, `methodology.md`, `data/`, `analysis/`, `results.md`
3. Update `experiments/README.md`

**New figure?**
1. Add to appropriate subfolder: `figures/conceptual/` or `figures/data/`
2. Include source files (SVG preferred)
3. Update `figures/README.md` with description

**New documentation?**
1. Add to `docs/`
2. Link from main `README.md` if relevant
3. Keep accessible (avoid jargon, explain technical terms)

### Modifying Existing Content

**Paper updates:**
- Minor fixes: Edit `paper/computational_substrates.md` directly
- Major revisions: Create `paper/revisions/v1.X_summary.md` + new version
- Keep old versions for reference

**Prediction protocols:**
- Create `protocol_v2.md` if significant changes
- Document rationale for changes
- Update `README.md` to note latest version

**Experimental results:**
- Never delete raw data
- Add new analyses as separate files
- Document any corrections/updates in `README.md`

---

## 📊 Size Guidelines

### Keep Files Manageable
- **Short docs**: < 2,000 words (quick reference)
- **Medium docs**: 2,000-10,000 words (detailed guides)
- **Long docs**: > 10,000 words (comprehensive papers)

If a file exceeds these guidelines, consider splitting:
- `paper/computational_substrates.md` is intentionally long (40,000 words) - the main scholarly work
- But split supplementary material into `paper/supplementary/`

### Data Files
- Raw data: Keep in CSV or similar open format
- Large files (>10MB): Consider external hosting (Zenodo, OSF) and link
- Include data dictionary explaining variables

---

## 🔍 Finding Things

### For Specific Needs

**I want to understand the framework:**
→ Start with `README.md`, then `paper/computational_substrates.md`

**I want to test a prediction:**
→ Go to `predictions/`, pick one, read `protocol.md`

**I need accessible explanation:**
→ Check `docs/`, start with `glossary.md` and `key_insights.md`

**I want to cite this work:**
→ See `assets/citation.bib` or citation in `README.md`

**I want to see the data:**
→ When available, go to `experiments/[name]/data/`

**I want to use the code:**
→ Check `predictions/[name]/code/` for simulations
→ Check `experiments/[name]/analysis/` for analysis code

### Search Tips

**GitHub's search is powerful:**
- Search within this repo: `repo:HillaryDanan/computational-substrates [query]`
- Search in code: Include language, e.g., `language:Python energy measurement`
- Search in issues/discussions: `is:issue [query]`

---

## 📝 Maintenance

### Regular Updates
- Update `STRUCTURE.md` when adding major new sections
- Update `README.md` roadmap quarterly
- Update `predictions/README.md` as predictions are tested
- Keep `references/bibliography.bib` current with new citations

### Version Control
- Main paper: Significant updates warrant version tags (v1.0, v1.1, etc.)
- Experimental protocols: Version in filename if changed (`protocol_v2.md`)
- Code: Use semantic versioning (v0.1.0, v0.2.0, v1.0.0)

### Deprecation
- Don't delete deprecated content—move to `archive/` folder
- Mark deprecated files with banner: `**⚠️ DEPRECATED - See [new location]**`
- Keep for historical reference and reproducibility

---

## 🎯 Design Philosophy

**1. Clarity > Cleverness**
- Use obvious names, not clever abbreviations
- Write self-documenting file structures
- Explain non-obvious choices

**2. Accessibility > Exclusivity**
- Lower barriers to entry
- Multiple entry points for different audiences
- Plain language where possible

**3. Reproducibility > Brevity**
- Include all details needed to reproduce
- Better to over-document than under-document
- Future you will thank present you

**4. Evolution > Perfection**
- Start simple, grow as needed
- Structure can evolve—don't over-plan
- Document changes when structure shifts

---

## 🚀 Future Considerations

As this repository grows, we may add:

**Community Features:**
- `discussions/` - FAQ, ideas, questions
- `contributors.md` - Acknowledge contributors
- `changelog.md` - Track significant changes

**Educational Content:**
- `tutorials/` - Step-by-step guides
- `lectures/` - Slide decks or recorded presentations
- `workshops/` - Hands-on exercises

**Applications:**
- `tools/` - Software packages built from this framework
- `demos/` - Interactive demonstrations
- `case_studies/` - Real-world applications

**Collaboration:**
- `collaborations/` - Joint work with other researchers
- `replications/` - Others testing our predictions
- `extensions/` - Novel applications of framework

**We'll add these as needed—not prematurely.**

---

## ❓ Questions?

If this structure is unclear or you're not sure where something belongs:

1. Check if similar content already exists (use GitHub search)
2. Ask in [Discussions](../../discussions) or [Issues](../../issues)
3. Propose structure changes (PRs welcome!)
4. When in doubt, document your reasoning in a README.md

**Principle:** If you're confused about where something goes, others will be too. Better to ask than to guess.

---

## 📊 Structure Health Metrics

We'll track (informally):
- **Discoverability**: Can people find what they need?
- **Completeness**: Are folders/files sufficiently documented?
- **Consistency**: Do we follow our own conventions?
- **Accessibility**: Can non-experts navigate successfully?

**Feedback welcome!** This structure serves the content—if it's not working, we'll change it.

---

**Structure designed for:** Clarity, growth, collaboration, and reproducibility.

**Structure evolves with:** New content, community needs, and lessons learned.

**Structure serves:** The core mission of making substrate-aware intelligence accessible, testable, and impactful.

---

*Last updated: November 14, 2025*  
*See git history for structure evolution*
