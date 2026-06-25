
# UNIVERSE 69 — Role-Play Game (18+) with UNO Mechanics

**A research tool packaged as a tabletop game**

**Version:** 1.0  
**Status:** Game Design Document (GDD)
## 🏷️ Topics
card-game, game-design, game-design-document, role-playing-game-system, applied-psychoanalysis, sexology-research, adult-gaming, projective-technique, psychology-research, behavioral-science, research-methodology, group-dynamics, narrative-design, shadow-work, roleplay-framework, bivrest-protocol, social-validation, therapeutic-games, affective-computing, emotion-recognition, behavioral-data-collection, experimental-protocol, llm-training-data, ai-training-data
---

## 📑 Table of Contents

- [The Problem](#-the-problem)
- [What UNIVERSE 69 Offers](#-what-universe-69-offers)
- [What UNIVERSE 69 Actually Does](#-what-universe-69-actually-does)
- [Who UNIVERSE 69 Is For](#-who-universe-69-is-for)
- [How the Game Works](#-how-the-game-works)
- [Data Structure](#-data-structure)
- [Quick Start](#-quick-start)
- [Integration with BIVREST Protocol](#-integration-with-bivrest-protocol)
- [Limitations](#-limitations)
- [Citation](#-citation)
- [Contacts](#-contacts)

---

## The Problem

In role-playing games and research sessions, it's difficult to create a structured environment that simultaneously:

- **Triggers spontaneous role-play behavior**
- **Provides repeatable conditions** for comparison
- **Collects data** in a unified format
- **Bypasses psychological defenses** of participants

**What researchers and facilitators face:**

| Method | Problem |
| :--- | :--- |
| **Free-form role-play** | No clear rules; players break character; data is incomparable |
| **Surveys and interviews** | Social desirability bias; participants say what's "acceptable" |
| **Standardized tests** | Don't elicit spontaneous behavior; detached from real context |
| **Natural observation** | Data is hard to structure; no repeatability |

**The result:** researchers spend time on preparation but get incomparable data, while participants cannot fully immerse in the role-play experience.

---

## What UNIVERSE 69 Offers

UNIVERSE 69 is a **session kit for conducting role-playing games** that solves these problems through:

1. **Strict UNO structure** — every move is tied to game rules; players cannot "drift" out of character
2. **Card tasks** — 54 tasks of varying difficulty that trigger spontaneous reactions
3. **Roles (avatars)** — psychological archetypes for role-play
4. **BIVREST protocol** — built-in data collection mechanism with binary labeling

**The core idea:**

Instead of asking participants: *"How did you feel in your role?"* — the game creates conditions where they **naturally display role-play behavior**. The group then votes on whether that behavior was congruent.

This **shifts the focus** from self-report to **observable behavior** and generates data that can be statistically analyzed.

---

## What UNIVERSE 69 Actually Does

**Important:** UNIVERSE 69 is not a therapeutic method or a ready-made AI solution. It is a **research tool**.

| What UNIVERSE 69 provides | What UNIVERSE 69 does NOT provide |
| :--- | :--- |
| A ready-made structure for role-play | A definitive answer to "was it played well?" |
| An experimental environment with repeatable rules | A clinically validated therapeutic method |
| A data collection protocol via BIVREST | Automatic dataset generation |
| Comparability across sessions with fixed rules | A turnkey commercial AI solution |

**UNIVERSE 69 is a tool for studying role-play behavior, group dynamics, and emotional responses in a structured environment.**

It is useful if your research question is:

- "How do people behave in tightly constrained role-play conditions?"
- "What types of tasks trigger congruent/incongruent behavior?"
- "How does the group perceive different role-play performances?"
- "Can labeled data about role-play behavior be collected through games?"

---

## Who UNIVERSE 69 Is For

| Audience | Purpose |
| :--- | :--- |
| **Psychologists, psychotherapists, sexologists** | A ready-to-use tool for group work with roles and projections. Rules, cards, roles, scenarios — everything "out of the box." |
| **Behavioral, narrative, and group dynamics researchers** | An experimental environment with repeatable rules and a data collection protocol (BIVREST) to study group dynamics, congruence, and the impact of tight constraints on creativity. |
| **Adult players (18+)** | A structure for deep role-play with clear rules and tasks of varying difficulty. |
| **AI/ML engineers (Affective Computing, Emotion Recognition)** | A labeled data collection protocol (logs with binary "Believe/Don't Believe" labels) for training models that assess social appropriateness, congruence, or trust in a character. |

---

## How the Game Works

### Game Participants

| Role | Description |
| :--- | :--- |
| **Players** | 2–9 people, 18+, each chooses an avatar (role) |
| **Dealer** | Manages the deck, enforces rules, records results |
| **Group** | Votes after each action via the BIVREST protocol |

### Game Loop

**Choose a role → Receive 6 cards and 6 "Chance" tokens → Play a card (UNO rules) → Role-play the card's task → Group verification (BIVREST) → Draw back up to 6 cards**

### Game Components

| Component | Description |
| :--- | :--- |
| **Rules** | Full game rules, loop, mechanics |
| **Cards** | 54 cards with tasks of varying difficulty |
| **Roles (avatars)** | Psychological archetypes for role-play |
| **Scenarios** | 9 psychological scenarios for analyzing game patterns |
| **BIVREST Protocol** | "Believe/Don't Believe" voting and logging |
| **LLM Prompt** | For solo play with AI |

### Card Matrix (by difficulty level)

| Range | Difficulty | Example Tasks |
| :--- | :--- | :--- |
| 2–5 | Low (warm-up) | Compliments, cocktails, stories, pantomime |
| 6–9 | Medium (unfolding) | Avatar presentation, fantasies, hugs, submission |
| 10–Ace | High (depth) | Sensations, experiments, undressing, domination |
| Joker | Maximum (chaos) | Complete rule-breaking |

**Full list of 54 cards with tasks — in `play/cards.md`**

### Distribution by Psychological Scenarios

| # | Scenario | Cards |
| :--- | :--- | :--- |
| 1 | Experimentation | 16 |
| 2 | Domination / Submission | 8 |
| 3 | Partner Replacement | 2 |
| 4 | Group Sex | 1 |
| 5 | Observation | 2 |
| 6 | Rape (archetype) | 1 |
| 7 | Idyllic Encounter | 15 |
| 8 | Sadomasochism | 4 |
| 9 | Socially Acceptable Deviations | 12 |

**Detailed scenario matrix — in `design/mechanics.md`**

---

## Data Structure

### Log Format (via BIVREST)

| Field | Type | Description |
| :--- | :--- | :--- |
| `session_id` | string | Session identifier |
| `round` | integer | Round number |
| `player_id` | string | Player identifier |
| `avatar` | string | Player's role |
| `task` | string | Card task |
| `action_text` | text | Role-play output (what was said/done) |
| `votes_believe` | integer | Number of "Believe" votes |
| `votes_dont_believe` | integer | Number of "Don't Believe" votes |
| `verdict` | string | "Believe" or "Don't Believe" |
| `tokens_lost` | integer | How many tokens were lost |
| `empty_chair` | boolean | Was there a break from role |

**Example log:** `play/logs.md`

---

## 🚀 Quick Start

### 1. Download the materials

This repository contains everything needed for a game session.

### 2. Read the key documents

- **Game Rules** (`play/rules.md`) — detailed rules and game loop
- **Card Deck** (`play/cards.md`) — 54 cards with tasks
- **Roles (Avatars)** (`play/avatars.md`) — role registry (Light / Hard)
- **Scenario Matrix** (`design/mechanics.md`) — 9 psychological scenarios
- **Example Logs** (`play/logs.md`) — what completed data looks like

### 3. Run a session

#### Group Play (2–9 players)

1. Gather your group (18+), choose a dealer
2. Print cards from `play/cards.md` and avatars from `play/avatars.md`
3. Deal **6 cards** and **6 "Chance" tokens** to each player
4. Each player chooses an avatar
5. Follow the rules in `play/rules.md`
6. Record results via BIVREST

#### Solo Play (1 player with LLM)

1. Open `play/solo-prompt.md`
2. Copy the entire prompt
3. Paste it as the first message in ChatGPT, DeepSeek, or Claude
4. Play against the AI opponent

### 4. Analyze the data

The collected logs enable:

- **Quantitative analysis** — frequencies, distributions, dynamics
- **Comparative analysis** — between different roles, players, sessions
- **Model training** — if you are collecting data for AI

---

## Integration with BIVREST Protocol

UNIVERSE 69 and **BIVREST** are two complementary projects:

- **UNIVERSE 69** creates the context and triggers behavioral responses
- **BIVREST** evaluates these responses by the group ("Believe/Don't Believe") and records results in a log

### How BIVREST is Embedded in UNIVERSE 69

| UNIVERSE 69 Mechanic | Role in BIVREST |
| :--- | :--- |
| **Cards with tasks** | Generate information for evaluation (stage I) |
| **Avatars (roles)** | Provide context for congruence assessment |
| **"Believe/Don't Believe" voting** | Core verification mechanism (stage B) |
| **"Chance" tokens** | Resource lost on "Don't Believe" |
| **"Empty chair"** | Break from role after repeated "Don't Believe" |
| **Logging** | Recording of all actions and votes |

**Link to project:** [BIVREST on GitHub](https://github.com/olesyalazareva/bivrest-method)

---

## Limitations

- **Game-based evaluation ≠ objective truth** — the result reflects group perception, not absolute reality
- **Rules must be fixed** — changing rules makes data incomparable
- **Multiple sessions required** — for statistically significant data
- **Social desirability doesn't disappear** — it transforms into a desire to meet group expectations
- **Not a certified therapeutic method** — a tool for observation and data collection, not a clinical protocol

---

## Citation

```bibtex
@misc{lazareva2025universe69,
  author = {Lazareva, Olesya},
  title = {UNIVERSE 69: Role-Play Game for Behavioral Research and Affective Computing},
  year = {2025},
  url = {https://github.com/olesyalazareva/universe69},
  note = {Applied psychoanalysis and sexology framework for LLMs}
}
Contacts
Olesya Lazareva
Psychoanalyst-Sexologist, Game Technician with 25 years of experience

Telegram: @olesyalazarevalove

Email: psi-tech@yandex.com

For commercial licensing inquiries: Telegram only

License and Terms
Non-commercial use (academic research, open-source projects) — free with attribution and a link to this repository

Commercial use (selling solutions based on UNIVERSE 69, corporate deployments) — by agreement with the author

⭐ If this project is useful for your work, please star the repository — so other researchers and developers can find it.



---

