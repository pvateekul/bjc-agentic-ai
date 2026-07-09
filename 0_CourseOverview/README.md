# Prompt Engineering & Agentic AI Notes

A concise reference for effective prompting techniques and Agentic AI concepts.

---

# Prompt Engineering

## 1. System Prompt

Defines the AI's role, behavior, expertise, and constraints before processing user requests.

### Components
- **System Prompt** — Who the AI is, responsibilities, rules
- **User Prompt** — The user's instruction or question

### Variants

#### 1.1 Without a System Prompt
Only the user instruction is provided.

```text
User: Explain machine learning.
```

#### 1.2 With a System Prompt
A system role is established before the user instruction.

```text
System:
You are a senior machine learning instructor. Explain concepts clearly with practical examples.

User:
Explain machine learning.
```

**Benefits**
- More consistent responses
- Better control over style and behavior
- Reduces ambiguity

---

# 2. Guideline Prompting (ICIO)

ICIO provides structure so the AI understands exactly what is expected.

## ICIO Framework

| Component | Meaning |
|-----------|---------|
| **Instruction** | What to do |
| **Context** | Background information |
| **Input** | Data to process |
| **Output** | Desired response format |

### Example (Naive)

```text
Summarize this article.
```

### Example (ICIO)

```text
Instruction:
Summarize the article.

Context:
Audience is university students.

Input:
<article>

Output:
- Bullet points
- Maximum 5 bullets
- Simple language
```

**Benefits**
- Clear expectations
- Higher-quality responses
- Better consistency

---

# 3. Structured Output

Specify the exact output format rather than letting the AI choose.

## Examples

### CSV

```text
Return the result as CSV with these columns:

Name, Age, Occupation, Country, Salary
```

### JSON

```json
{
  "name": "",
  "age": "",
  "occupation": ""
}
```

### Markdown Table

```text
Return the answer as a Markdown table.
```

**Benefits**
- Easier parsing
- Consistent formatting
- Better integration with software

---

# 4. Check Conditions (Reduce Hallucinations)

Prevent the model from inventing information.

## Example

```text
Answer only using the provided content.

Do not add information that is not explicitly stated.

If the answer does not exist, return:
null
```

Alternative:

```text
If the information is unavailable, answer:
"ไม่มี"
```

**Purpose**
- Reduce hallucination
- Increase reliability
- Ensure factual outputs

---

# 5. Reasoning Prompting

Encourage the model to spend additional effort reasoning before producing the final answer.

## Example Problem

```text
Calculate:

7 + 8 × 2 − 5 + 3 × 2
```

Correct evaluation:

```
7 + 16 − 5 + 6
23 − 5 + 6
18 + 6
24
```

### Request Reasoning

```text
Solve the problem and explain your reasoning before giving the final answer.
```

### Numbered Steps

```text
1. Multiply first.
2. Perform addition and subtraction from left to right.
3. Compute the final value.
```

> **Note:** The model may not always reveal its internal reasoning. When you need transparency, ask for an explanation or solution steps rather than requesting hidden reasoning.

---

# 6. Few-Shot Prompting

Provide examples so the AI learns the expected pattern.

## Zero-Shot

No examples.

```text
Translate:

Hello
```

---

## One-Shot

One example.

```text
Example

Input:
Dog

Output:
สุนัข

Now translate:

Cat
```

---

## Few-Shot

Multiple examples.

```text
Input:
Dog

Output:
สุนัข

Input:
Cat

Output:
แมว

Input:
Bird

Output:
นก
```

**Benefits**
- Improves consistency
- Handles formatting better
- Useful for specialized tasks

---

# Agentic AI

Traditional AI primarily answers questions.

Agentic AI can **plan, execute, and automate tasks**, often by using tools, code execution, and workflows.

---

## 1. File Organization

### Direct Execution

```text
Organize all files into folders by file type.
```

The agent performs the task immediately.

### Plan Mode

```text
Create a plan for organizing my files.
Wait for my approval before making changes.
```

The agent first proposes a plan before execution.

---

## 2. Data Analysis Workflow

Example task:

```text
Analyze file.csv.

Generate:
- Summary report
- Charts
- Insights
```

Potential reusable assets:

### `SKILL.md`

Reusable procedures or capabilities that can be shared across projects.

Example:

```text
CSV Analysis Skill

Steps:
1. Load CSV
2. Clean data
3. Generate statistics
4. Create visualizations
5. Produce report
```

Example scheduled workflow:

```text
@QA_w_Visual
```

Runs automated quality assurance with visual outputs on a schedule.

---

## 3. `AGENTS.md`

Defines how AI agents should behave within a project.

Typical contents:

- Responsibilities
- Goals
- Constraints
- Available tools
- Coding standards
- Workflow rules

### Scope

#### Global

Applies across the entire organization or repository.

#### Local

Applies only to a specific project or directory.

---

## 4. Multi-Agent Systems

Instead of one AI doing everything, multiple specialized agents collaborate.

Example architecture:

```text
Planner Agent
        │
        ▼
Coder Agent
        │
        ▼
Tester Agent
        │
        ▼
Reviewer Agent
        │
        ▼
Final Report
```

**Advantages**
- Separation of responsibilities
- Better scalability
- Parallel execution
- Higher reliability
- Easier maintenance

---

# Summary

| Topic | Purpose |
|--------|---------|
| System Prompt | Define AI role and behavior |
| ICIO | Structure prompts clearly |
| Structured Output | Specify exact response format |
| Check Conditions | Reduce hallucinations |
| Reasoning Prompting | Encourage step-by-step explanations when appropriate |
| Few-Shot Prompting | Teach patterns through examples |
| Agentic AI | Enable planning and task execution |
| SKILL.md | Store reusable capabilities |
| AGENTS.md | Define agent behavior and responsibilities |
| Multi-Agent | Coordinate multiple specialized AI agents |