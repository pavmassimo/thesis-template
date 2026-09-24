# TinyML Research Project Template

A minimal, collaborative template for rigorous on-device learning research projects developed with AI agents and human feedback.

## Folder Structure

```
.
├── papers/              # Literature review and reference management
│   └── papers.csv       # Structured list of papers (author, title, year, link)
├── experiments/         # Experiment runs, configs, logs, results
├── data/                # Raw and processed data (never committed)
├── thesis/              # Thesis writing and final outputs
├── agent.md             # Guidelines for working with AI agents
└── README.md            # This file
```

## Workflow

1. **Literature Review** — Read papers, record in `papers/papers.csv`, synthesize key findings
2. **Research Design** — Define clear research questions/objectives, establish baselines
3. **Experiments** — Run reproducible experiments, log everything in `experiments/`
4. **Iterate** — Analyze results, refine questions, go back to 2 or 3
5. **Write Thesis** — Distill findings into clear, concise thesis format

## Key Principles

- **Version control is default** — Use git to track your work, commit regularly
- **Reproducibility first** — Log environments, hyperparameters, random seeds, data splits
- **Learning over perfection** — Failed experiments are learning; understand *why* they failed
- **Concise writing** — Clear, direct, no fluff; thesis should map to your experimental work
- **Collaborate** — Use agents to question assumptions, check rigor, brainstorm next steps

## Getting Started as a Student

**This is a public template.** You'll create your own private repository for your research work.

### Setup Steps

1. **Clone this template locally:**
   ```bash
   git clone https://github.com/massimopinto/thesis-template.git
   cd thesis-template
   ```

2. **Create a new private GitHub repository** for your project:
   - Go to [github.com/new](https://github.com/new)
   - Name: something descriptive (e.g., `2026-surname-ondevicelearning4anomalydetection`)
   - **Make it PRIVATE** (only you and Massimo can see it)
   - Do NOT initialize with README, .gitignore, or license (you already have these)
   - Click "Create repository"

3. **Update the origin and push your local copy:**
   ```bash
   git remote remove origin
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
   git branch -M main
   git push -u origin main
   ```

4. **Share your repo with Massimo:**
   - Go to Settings → Collaborators (on your GitHub repo)
   - Add Massimo's GitHub username with at least "Write" access
   - (Massimo will share the correct username/details)

5. **Start working:**
   - Create environment specs (requirements.txt or conda.yml) and commit
   - Add papers to `papers/papers.csv`
   - Start your first experiments in `experiments/`
   - Read `agent.md` to understand how to work with AI agents

### Tips

- **Commit often** — Small, clear commits help track your progress
- **Write clear commit messages** — "Add baseline experiment with MobileNetV2" beats "update"
- **Use branches** for experiments if you're testing multiple approaches
- **Keep data/ out of git** — It's in .gitignore; use external storage if needed
- **Collaborate early** — Share your repo link with Massimo and agents as soon as you have a baseline

## Working with Agents

See `agent.md` for guidelines on what agents should ask, how to handle failures, and how to keep experiments rigorous and reproducible.

Do not accept everything the agent proposes; be critical of their suggestions and their work. Always remember the objective of each experiment, check the output before anything else: your results are YOUR responsibility, not your agents.  