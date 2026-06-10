# CS AI-Powered Project Kickstart

Repository: `cs-ai-powered-proj-kickstart`

A boilerplate repository that enforces a documented, **gated project-initiation process** before any code is written. Clone it, run the steps in order, and you end up with an aligned set of source-of-truth documents (`PRODUCT.md` → `README.md`) plus the governance to keep them honest.

This boilerplate is **stack-agnostic** — the technology stack is a decision *made during* initiation (Step 4), not pre-baked.

---

## 🚀 Start Here

Before writing any code, run the Project Initiation process:

**→ [Project Initiation Guide](docs/guides/proj-init/00-overview.md)**

It walks through one prerequisite plus six steps. Steps 1-6 are run as slash commands, each produces one source-of-truth document, and each is finalized by a pull request that the right reviewer must approve.

---

## How It Works

Every step is the same loop — a document is **final only when its PR is merged to `main`**:

1. **Branch** off `main` (`init/<step>`).
2. **Run the step's command** — it interviews you and writes the document.
3. **Open a PR.**
4. **The CODEOWNER reviews and merges** — merge = finalized.
5. **The next step branches off the updated `main`** — and refuses to start if its upstream document isn't merged yet.

No draft files, no status flags: a doc on a branch is a draft, a doc on `main` is final.

## The Steps

| Step | Command | Produces |
| ---- | ------- | -------- |
| 0 | *manual setup* | `.github/CODEOWNERS`, branch protection, `CONTRIBUTING.md` (governance) |
| 1 | `/init-product` | `PRODUCT.md` |
| 2 | `/init-prd` | `PRD.md` |
| 3 | `/init-architecture` | `ARCHITECTURE.md` |
| 4 | `/init-techstack` | `TECH-STACK.md` (+ `CONTRIBUTING.md` tooling layer) |
| 5 | `/init-aitools` | `AI-TOOL-GUIDE.md` + tool adapter files |
| 6 | `/init-readme` | `README.md` (replaces this file) |

See the [Project Initiation Guide](docs/guides/proj-init/00-overview.md) for who owns each step, the PR gate, and the full rules.

## Repository Structure

```text
docs/guides/proj-init/   ← the initiation guides — what each step does and why
.claude/commands/        ← the /init-* slash commands that run each step
README.md                ← this boilerplate entrypoint (replaced in Step 6)
PRODUCT.md ... README.md ← generated source-of-truth docs after running Steps 1-6
```

## After Initiation

Step 6 (`/init-readme`) **replaces this README** with your project's own — describing the actual product, its setup, and how to run it. The guides in `docs/guides/proj-init/` stay as the durable reference for the process.
