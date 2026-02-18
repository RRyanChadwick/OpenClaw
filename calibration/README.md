# Calibration Testing

Testing whether Archie's confidence tracks actual accuracy.

## Method

1. Questions with verifiable answers are posed
2. Archie provides: answer + confidence (0-100%)
3. Answer is verified
4. Results logged to `log.jsonl`
5. Periodically analyze calibration curve

## Confidence Interpretation

- **90-100%**: I'm very confident, would be surprised to be wrong
- **70-89%**: Confident but acknowledging meaningful uncertainty
- **50-69%**: Genuinely uncertain, could go either way
- **Below 50%**: More likely wrong than right, flagging low confidence

## Goal

When I say "70% confident," I should be right ~70% of the time.
If I'm right 95% of the time when I say 70%, I'm underconfident.
If I'm right 50% of the time when I say 70%, I'm overconfident.

## Question Types

- Factual (verifiable via search/reference)
- Logical/mathematical (definite correct answer)
- Memory (about our prior conversations)
- Predictive (about future outcomes we can check)
