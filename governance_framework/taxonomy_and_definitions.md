# AI Safety & Transparency: Taxonomy and Definitions
Version 0.1 | Internal Editorial Standard

## Overview
To ensure consistency across all technical documentation, safety reports, and public-facing transparency disclosures, the following definitions must be used. These terms are prioritized for clarity, technical accuracy, and removal of ambiguity.

## Core Safety Concepts

### 1. Model Alignment
**Definition:** The process of ensuring that an AI system’s goals and behaviors remain consistent with human intent and safety requirements.

*Ed note: Avoid ambiguities around similar words, like using "alignment" as a synonym for "training." Here "alignment" refers specifically to the *objective* of the training, not the mechanics of the process.*

### 2. Hallucination
**Definition:** A phenomenon where an AI model generates output that is factually incorrect, nonsensical, or unsupported by its training data/context based on patterns and/or objects that do not exist. Also sometimes referred to as confabulation or delusion.

*Ed note: When describing hallucinations in safety reports, specify whether the hallucination is factual (incorrect dates/names), logical (broken reasoning), procedural (ignoring instructions), or perceptual (details imperceptible to humans).*

### 3. Frontier Models
**Definition:** AI models pushing the boundaries of current capability in terms of scale, reasoning, and/or multi-modality, requiring specialized safety oversight due to potential impact.

*Ed note: Use *frontier* specifically when discussing high-compute, large-scale systems. Do not use it as a general descriptor simply for powerful AI models, or all cloud- or service-based models.

### 4. Red Teaming
**Definition:** The practice of intentionally probing an AI system to identify vulnerabilities, safety failures, or unintended behaviors in a controlled environment.

*Ed note: Distinguish between automated red teaming (purely scripted attacks) and human-in-the-loop red teaming (adversarial human testing, which can be more nuanced).*

### 5. Interpretability
**Definition:** The degree to which the internal mechanics, weights, or decision-making processes of a model can be properly understood by humans.

*Ed note: When discussing black box models, clarify if you are referring to *mechanistic interpretability* (understanding neurons/weights) or *behavioral interpretability* (predicting outputs based on inputs).*

### 6. Data Contamination
**Definition:** The inclusion of test data, evaluation benchmarks, or specific private information within a model’s training corpus, potentially leading to a host of problems, such as skewed performance metrics or amplified biases.

*Ed note: This is a critical term for transparency reports; ensure the distinction between intentional contamination and unintentional leakage is clear.*

## Human Impact & Stability Risks

### 7. Model Instability / Erratic Behavior
**Definition:** Instances where a model produces inconsistent, nonsensical, or rapidly degrading outputs that deviate from established safety boundaries or logical patterns.

*Ed note: Distinct from *hallucination*, use this term to describe the psychosis-like behaviors (such as repetitive loops, sudden shifts in tone, or incoherent reasoning) without using non-technical metaphors.*

### 8. Societal Harm & Bias
**Definition:** The risk that an AI system produces outputs that reinforce systemic prejudices, spread misinformation, or contribute to discriminatory outcomes in real-world applications.

*Ed note: When discussing this, it's always best to specify the specific type of harm in question (e.g., *algorithmic bias in hiring practices* vs. *generative misinformation in news cycles*) since they can vary wildly in domain and scope.*

### 9. Human-in-the-Loop (HITL) Safeguards
**Definition:** Human oversight into an AI system's workflow that seeks to validate, correct, or override model outputs *before* they reach a user (ironically taking human time to ensure safety in automations intended to save human time).

*Ed note: This is currently a primary industry safety mechanism, helping particularly with edge cases where model training can fail. When discussing harm prevention, focus on where and how HITL is deployed as a failsafe.*

### 10. Cognitive Dependency (or Human Agency Degradation)
**Definition:** The risk that increased reliance on AI for complex reasoning, creative synthesis, or decision-making leads to a measurable reduction in human cognitive proficiency, critical thinking skills, and independent agency.

*Ed note: Distinguish between *supplemental usage* (using AI as a tool to augment a human's capability) and *substitutive usage* (allowing the AI to replace the underlying thought process). The goal of safety frameworks should be to promote the former while mitigating the risks of the latter insofar as possible.*

## Technical & Systemic Risks

### 11. Information Integrity (Misinformation/Disinformation)
**Definition:** The risk that an AI system generates, amplifies, accelerates, or facilitates the spread of false, misleading, or deceptive content at scale, whether through fabricated references, parroting of bad information, or generated images and audio passed as real.

*Ed note: Distinguish between unintentional errors (hallucinations) and deliberate manipulation (disinformation). This is a key distinction for safety policy.

### 12. Privacy & Data Leakage
**Definition:** The risk that an AI system inadvertently reveals personally identifiable information (PII), proprietary data, or sensitive training content in its outputs.

*Ed note: Use *data leakage* when referring to the technical failure of a model's boundaries, and *privacy violation* when referring to the resulting impact on individuals or other entities.*

### 13. Dual-Use Risks
**Definition:** The risk that AI features developed for benign or beneficial purposes (such as chemical research, image generation, or coding) can be directly used for harmful ends (like bioweapon development, disinformation, or cyberattacks).

*Ed note: This is a critical term in frontier model safety especially, highlighting the need for access controls and capability monitoring.*

## 14. Long-Horizon Model Autonomy
**Definition:** The risks associated with AI systems designed to perform tasks autonomously over extended periods, where multi-step reasoning and persistent goal-seeking can lead to unexpected and unwanted behaviors, environmental manipulation, or *drift* from ostensibly rigid safety constraints.

*Ed note: Contrast this with *short-horizon* models, generally designed to generate a single response, or even conser-grade agentic models. For long-horizon systems, focus on cumulative error and agentic drift, where small deviations in early steps compound into significant, unintended consequences by the end of a task (or over the course of multiple tasks).*

### Style & Usage Guidelines

**Precise Attribution:** When describing failures or risks, be sure to clearly identify both the *actor* (model vs. human) and the *mode of occurrence* (inherent capability vs. external influence); for example, distinguish between a model's inherent tendency to hallucinate and an external user’s intentional prompt injection.

**Neutrality:** Maintain a neutral, objective tone. Avoid alarmist adjectives and adhere to journalistic or academic restraint (e.g., using a term like "significant risk" instead of "shocking danger").

**Precision:** If a term is not defined in this taxonomy, then it *must* be contextualized upon first use.

## Further Reading

**Data Contamination - **
https://www.holisticai.com/blog/overview-of-data-contamination
**HITL - **
https://www.ibm.com/think/topics/human-in-the-loop
**Information Integrity - **
https://www.rand.org/pubs/perspectives/PEA3089-1.html
**Long-Horizon Model Safety - **
https://openai.com/index/safety-alignment-long-horizon-models/