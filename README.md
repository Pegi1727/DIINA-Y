markdown
# DIINA-Y: Tonal Language NLP
Framework for Yoruba language disambiguation using Inhibitory Control.
Author: Dr. Pegah Merrikhi
markdown
---
## Research Abstract
‌
**Title:** DIINA-Y: A Neuro-Inhibitory Computational Framework for Tonal Disambiguation in Low-Resource Yorùbá Corpus
‌
**Abstract:**
The disambiguation of tonal variations in Yorùbá remains a formidable challenge for contemporary Neural Machine Translation (NMT) and Natural Language Understanding (NLU) systems. This paper introduces **DIINA-Y** (Dynamic Inhibition-Inspired Neural Architecture for Yorùbá), a novel computational architecture predicated on the principle of **Inhibitory Control Mechanisms**.
‌
Unlike traditional attention-based models, DIINA-Y employs a **Dynamic Inhibitory Regulator (DIR)** module that actively suppresses contextually incongruent semantic candidates. Our methodology effectively mitigates 'tonal noise' by simulating selective suppression of sub-phonemic conflicts. Preliminary evaluations demonstrate a statistically significant improvement in resolving homographic ambiguities compared to baseline Transformer architectures.

```markdown
‌
---
### Methodology: The Dynamic Inhibitory Regulator (DIR)
‌
The core innovation of DIINA-Y lies in its non-linear inhibitory gating mechanism. While standard Transformer models utilize excitatory attention to prioritize features, DIINA-Y introduces a secondary Inhibitory Hidden Layer.
‌

Feature Extraction: Input Yorùbá tokens are embedded into a d-dimensional vector space.
Inhibitory Gating: The inhibitory signal (G_{inh}) is calculated as:
G_{inh} = \sigma(W_{inh} \cdot H_{t} + b_{inh})
(Where \sigma is the sigmoid activation function and H_{t} is the hidden state).
Contrastive Suppression: The final output is computed by:
H_{final} = H_{t} \odot (1 - G_{inh})
‌
This operation ensures that 'semantic noise'—specifically incorrect tonal interpretations—is actively suppressed before reaching the final classification layer.
```
