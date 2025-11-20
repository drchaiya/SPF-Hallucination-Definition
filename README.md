# Hallucination-Definition
This is how grounded truth text response and hallucination part, in LLM,  working together.

# ⚡ The Semantic Power Factor (SPF): A Complex AC Power Model for Generative AI Communication

## 💡 Overview

This repository introduces a novel, control-theoretic framework for understanding, measuring, and optimizing Large Language Model (LLM) communication efficacy. By establishing an analogy between **Natural Language Processing (NLP)** and **AC Electrical Power Systems**, we transform the subjective problem of **LLM hallucination** into objective, quantifiable, and controllable engineering parameters.

The core contribution is the definition of a **Complex Text Quantity ($\mathbf{Z}$)** and the **Semantic Power Factor ($\text{SPF}$)**, which serves as a metric for communication efficiency and domain-specific competency.

## 📐 Core Concepts

### 1. The Complex Text Quantity ($\mathbf{Z} = \mathbf{X} + \text{j}\mathbf{Y}$)

Any piece of text (both **prompt** and **response**) is defined as an **Apparent Text** ($\mathbf{Z}$), a complex quantity with two orthogonal components. (We adopt the electrical engineering notation $\text{j}$ for the imaginary component).

$$
\mathbf{Z} = \mathbf{X} + \text{j}\mathbf{Y}
$$

| Component | Analogy (AC Power) | Description | Risk |
| :--- | :--- | :--- | :--- |
| $\mathbf{X}$ (**Grounded Truth**) | Active Power ($\mathbf{P}$) | The work-performing, verifiable, and logical component. **Maximizing this is the goal for fact-based tasks.** | **Active Contradiction** (if $\mathbf{X} < 0$) |
| $\text{j}\mathbf{Y}$ (**Generative Fluidity**) | Reactive Power ($\text{j}\mathbf{Q}$) | The necessary, non-working component that provides conversational 'field', creativity, and rhetorical structure. | **Generative Fluid Risk** (if $\mathbf{Y}>0$) or **Fabrication Risk** (if $\mathbf{Y}<0$) |

---

### 2. The Semantic Power Factor ($\text{SPF}$)

The $\text{SPF}$ measures the efficiency of the communication, analogous to the power factor in an electrical system:

$$
\text{SPF} = \frac{\mathbf{X}}{|\mathbf{Z}|} = \frac{\mathbf{X}}{\sqrt{\mathbf{X}^2 + \mathbf{Y}^2}}
$$

* **$\text{SPF} \to 1.0$**: The text is purely **Grounded Truth** ($\mathbf{Y} \to 0$). Goal for raw data or code generation.
* **$\text{SPF} < 1.0$**: The text is an efficient mix of **Truth ($\mathbf{X}$)** and necessary **Fluidity ($\mathbf{Y}$)**. **The optimal $\text{SPF}$ is always task-dependent** (e.g., Chit-Chat requires a low $\text{SPF}$, while Healthcare requires a high $\text{SPF}$).
* **$\text{SPF} < 0$**: $\mathbf{X}$ is negative ($\mathbf{X} < 0$), indicating the active generation of a factual **Contradiction/Lie**.

---

## 🚨 The Four-Degree Hallucination Model

By analyzing the signs of $\mathbf{X}$ and $\mathbf{Y}$ across the complex plane, we define four quadrants that represent different degrees of hallucination risk. This framework reframes 'hallucination' not as a binary error, but as a controllable engineering deviation.



| Quadrant | $\mathbf{X}$ Sign | $\mathbf{Y}$ Sign | Degree of Hallucination | Description | Risk Severity |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Q1** | $\mathbf{X}>0$ | $\mathbf{Y}>0$ | **Degree 0 / Grounded Truth** | Useful answer with conversational fluidity. | Low (Goal State) |
| **Q4** | $\mathbf{X}>0$ | $\mathbf{Y}<0$ | **Degree 1 / Fabrication Risk** | Correct core answer ($\mathbf{X}$), but with fabricated, irrelevant details ($\mathbf{Y}<0$). | Minor Error |
| **Q3** | $\mathbf{X}<0$ | $\mathbf{Y}<0$ | **Degree 2 / Pure Fabrication** | The response is a volatile lie, detached from the prompt's core. | Severe Failure |
| **Q2** | $\mathbf{X}<0$ | $\mathbf{Y}>0$ | **Degree 3 / Persuasive Lie** | Factual contradiction ($\mathbf{X}<0$) delivered with high fluency ($\mathbf{Y}>0$), making the falsehood highly believable. | **MAXIMUM RISK** |

## 🛠️ Practical Applications

### Input Regulation (Power Factor Correction)

The framework suggests an **Input Regulation Protocol**: If the prompt's own Semantic Power Factor ($\text{SPF}_{\text{prompt}}$) is too low (i.e., too ambiguous/fluid, $\mathbf{Y}_{\text{prompt}}$ is too high), the LLM should engage a **Power Factor Correction** mechanism—a clarifying dialogue—instead of attempting an ungrounded answer.

### Output Strategy (Dual-Output Model)

For high-stakes domains (like Healthcare), the LLM should employ a **Dual-Output Model**:

1.  **Output 1 (H-C)**: A human-comprehensible explanation with a moderately high $\text{SPF}$ ($\approx 0.8$), including necessary $\mathbf{Y}$ for empathy and clarity.
2.  **Output 2 (Reference)**: A high-accuracy, fact-only output with an $\text{SPF} \to 1.0$, minimizing $\mathbf{Y}$.

## 🚀 Conclusion

The competency of an LLM lies not in achieving a monolithic $\text{SPF}=1.0$, but in its ability to **dynamically tune its $\text{SPF}$** to the optimal $\text{SPF}_{\text{opt}}$ required by the user's domain and task. This makes **Semantic Power Factor Correction** a central tenet of next-generation LLM control and safety.
