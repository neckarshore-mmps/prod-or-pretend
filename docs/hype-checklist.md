# Hype Detection Checklist

12 checkpoints for identifying hype posts on LinkedIn and X. Each checkpoint is scored on two dimensions:

- **Detectability (1-5):** How reliably can this be detected automatically?
- **Signal Strength (1-5):** How strongly does this indicate hype vs. substance?

## Checkpoints

| # | Checkpoint | Detectability | Signal | MVP | Example |
|---|-----------|---------------|--------|-----|---------|
| 1 | "Built this in a weekend" | 5 | 5 | Yes | Time-pressure claims without context |
| 2 | "Game changer" / "Revolutionary" | 5 | 4 | Yes | Superlatives without evidence |
| 3 | No link, repo, or demo | 4 | 5 | Yes | Claims without proof |
| 4 | "10x faster than X" without benchmark | 4 | 5 | Yes | Unsubstantiated performance claims |
| 5 | Engagement bait ("Thoughts?") | 5 | 3 | Yes | Algorithm-gaming phrases |
| 6 | Screenshot instead of live demo | 4 | 4 | Yes | Static proof vs. working software |
| 7 | "AI-powered" without explanation | 4 | 4 | Yes | Buzzword without substance |
| 8 | High likes, zero substantive comments | 3 | 4 | No | Engagement pattern analysis (harder to detect) |
| 9 | Same post from 3 months ago, repackaged | 2 | 5 | No | Content recycling (requires history tracking) |
| 10 | Buzzword density above threshold | 4 | 3 | Yes | Keyword frequency analysis |
| 11 | No mention of tests, security, scaling | 3 | 3 | No | Absence detection (requires deeper NLP) |
| 12 | "Just shipped" without proof | 5 | 4 | Yes | Launch claims without artifacts |

## MVP Scope

9 of 12 checkpoints are in MVP scope. Expected accuracy: ~80%. Calibrated in Phase 1 via human-in-the-loop feedback.

## Scoring

A post's hype score is the weighted sum of triggered checkpoints. Weighting TBD during calibration — signal strength is the starting weight.

**Threshold for analysis:** TBD. During Phase 1, all flagged posts are presented to the human operator for decision. Threshold is set based on observed false positive rate.

## Calibration Process

1. Hype detector runs against live feed
2. Human reviews each flagged post: true positive / false positive / missed
3. System logs decisions and adjusts weights
4. Target: ~99% accuracy before automating (Phase 2+)
