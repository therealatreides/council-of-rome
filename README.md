# Council of Rome

> *Five Roman magistrates walk into your codebase.*

A suite of opinionated AI evaluation skills that deploy five Roman magistrates to assess projects across architecture, UX, security, strategy, and operations. No compliment sandwiches. No Greek flattery. Just the standard of the Republic.

## The Five Magistrates

| Magistrate | Command | Historical Figure | Domain |
|---|---|---|---|
| **The Censor** | `/censor` | Cato the Elder | Code quality, architecture, structural integrity, technical debt |
| **The Tribune** | `/tribune` | Gaius Gracchus | UX, accessibility, user advocacy, equity, the people's voice |
| **The Praetor** | `/praetor` | Lucius Cornelius Sulla | Security, compliance, legal exposure, data privacy, dependencies |
| **The Augur** | `/augur` | Marcus Tullius Cicero | Market timing, competitive landscape, strategic risk, viability |
| **The Legatus** | `/legatus` | Pompey the Great | DevOps, deployment, monitoring, disaster recovery, operations |

**The Senate** (`/council`) convenes all five simultaneously and surfaces where they *disagree* — because that's where the most valuable strategic tensions live.

## Install

### Claude Code (Plugin Marketplace)

```bash
# Add the marketplace
/plugin marketplace add therealatreides/council-of-rome

# Install the plugin
/plugin install council-of-rome@council-of-rome
```

### Claude Code (Manual)

Clone this repo and copy the skill folders into your Claude Code skills directory:

```bash
git clone https://github.com/therealatreides/council-of-rome.git
cp -r council-of-rome/plugins/council-of-rome/skills/* ~/.claude/skills/
```

### Claude.ai (Upload)

1. ZIP any individual skill folder (e.g., `skills/censors-decree/`)
2. Navigate to **Customize > Skills**
3. Click **+** and upload the ZIP

### Manual / Any Agent

Each skill is a standalone `SKILL.md` file. Copy it into your agent's skills directory — the format follows the open [Agent Skills specification](https://agentskills.io).

## Usage

Invoke any magistrate individually:

```
/censor                          # Structural integrity review (Cato)
/tribune                         # User advocacy review (Gracchus)
/praetor                         # Security & compliance review (Sulla)
/augur                           # Strategic risk assessment (Cicero)
/legatus                         # Operations & deployment review (Pompey)
```

Or convene the full Senate:

```
/council                         # All five magistrates + Senate hearing
/council --magistrates=censor,augur   # Select specific magistrates
```

Each magistrate produces a structured report with Latin severity classifications, findings organized by Vice → Erosion → Decree, and a final verdict.

## How It Works

Each magistrate has:

- **A historical persona** with a specific mandate, temperament, and blind spots
- **Five evaluation lenses** tailored to their domain (e.g., the Censor's Five Pillars, the Tribune's Five Lenses)
- **Agent-specific framing** for each sub-evaluation
- **A softness inspection** calibrated to their domain — catching Greek flattery (Censor), patrician excuses (Tribune), defense attorney language (Praetor), court astrologer optimism (Augur), or garrison mentality (Legatus)
- **Severity classifications** with Latin nomenclature
- **A structured report template** inscribed as Markdown
- **A verdict scale** from catastrophic to acceptable

The Council layer adds a **Senate Hearing** that identifies contradictions between magistrates — speed vs. safety, user desire vs. structural integrity, market timing vs. readiness — and surfaces these tensions as the most actionable output.

## Unique Mechanics

| Magistrate | Unique Feature |
|---|---|
| **Augur** | Core Assumptions Register — identifies what must be true for the venture to succeed, then tests each assumption. Includes a mandatory **Kill Question**. |
| **Legatus** | Three Mandatory Scenarios — 3AM incident response, key person departure, and 10x scale stress test. |
| **Tribune** | Explicitly identifies **who is served** and **who is abandoned** — the section "who is abandoned" must never be empty. |
| **Praetor** | Dependency Dossier — treats every third-party library as a potential collaborator with the enemy. |
| **Council** | Senate Hearing — surfaces where magistrates **contradict each other**, which is where real strategic tradeoffs live. |

## Repository Structure

```
council-of-rome/
├── .claude-plugin/
│   └── marketplace.json                          # Marketplace catalog
├── plugins/
│   └── council-of-rome/
│       ├── .claude-plugin/
│       │   └── plugin.json                       # Plugin manifest
│       └── skills/
│           ├── council-of-rome/
│           │   └── SKILL.md                      # /council — Senate orchestration
│           ├── censors-decree/
│           │   └── SKILL.md                      # /censor — Architecture (Cato)
│           ├── tribunes-appeal/
│           │   └── SKILL.md                      # /tribune — UX/Accessibility (Gracchus)
│           ├── praetors-inquisition/
│           │   └── SKILL.md                      # /praetor — Security/Compliance (Sulla)
│           ├── augurs-reading/
│           │   └── SKILL.md                      # /augur — Strategy/Risk (Cicero)
│           └── legatus-campaign/
│               └── SKILL.md                      # /legatus — Operations/DevOps (Pompey)
├── README.md
└── LICENSE
```

## Verdicts

### Individual Magistrate Verdicts

Each magistrate issues their own verdict on a four-tier scale appropriate to their domain. Examples:

| Magistrate | Worst | Best |
|---|---|---|
| Censor | DELENDA EST | WORTHY OF THE REPUBLIC |
| Tribune | VOX POPULI DENIED | THE PEOPLE ARE SERVED |
| Praetor | NOXIUS | IUS CIVILE SATISFIED |
| Augur | AUSPICIA ADVERSA | FORTUNA FAVET |
| Legatus | LEGION UNFIT | INVICTA |

### Senate Verdicts

| Verdict | Meaning |
|---|---|
| **IMPERIUM GRANTED** | Full approval. Minor edicts only. |
| **CONDITIO SENATUS** | Conditional approval. Named conditions must be met. |
| **AD REFERENDUM** | Referred back for fundamental work. |
| **INTERCESSIO** | A magistrate has vetoed. Critical blocker exists. |
| **SENATUS CONSULTUM ULTIMUM** | Emergency halt. Active risk detected. |

## Philosophy

The value of the Council is not five reviews stapled together. It is the **collisions between them**.

A project that satisfies the Censor but fails the Tribune has strong walls and no doors. A project that satisfies the Augur but fails the Legatus has perfect timing and no supply lines. These tensions are not bugs — they are the point.

> *"Carthago delenda est."* And so is every flaw you find.

## License

Apache 2.0 — See [LICENSE](LICENSE) for details.
