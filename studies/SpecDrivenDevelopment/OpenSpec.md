# Spec-Driven Development (SDD) with OpenSpec

**Study reference:** [Beginner's Guide to Spec-Driven Development (SDD) With OpenSpec](https://youtu.be/9MImID9o8MQ?t=1414)

## 1. What is Spec-Driven Development?

Spec-Driven Development (SDD) is a software development approach in which specifications are created before implementation begins.

Instead of immediately asking an AI coding agent to implement something, we first define what we want to build, how it should behave, and what constraints it must follow.

The specification becomes the foundation for implementation.

### Why do we need it?

AI coding agents have a limited context window. This creates some challenges:

- **Context limitations:** An AI agent cannot keep an unlimited amount of information in its context window.
- **Multiple sessions:** Complex projects often require implementation across different conversations or sessions.
- **Context consistency:** Without persistent documentation, important decisions and requirements can be lost.
- **Unpredictable implementation:** Asking an AI to implement something without a clear specification can lead to inconsistent results.

SDD addresses these problems by introducing structured documentation that survives across sessions.

### Key principles

1. **Context engineering:** SDD is a form of context engineering. We organize and structure the information that AI agents need to perform their tasks.
2. **Single source of truth:** Specifications serve as the central reference for project requirements and decisions.
3. **Think before implementing:** Before starting development, define what needs to be built and document it.
4. **Session independence:** Development can happen across multiple sessions without relying entirely on previous conversation history.
5. **Structured implementation:** AI agents use specifications as guidance instead of relying exclusively on natural-language instructions.

---

## 2. Spec-Driven Development Frameworks

There are several frameworks and tools available to implement SDD workflows.

| Framework | Description |
|---|---|
| Spec Kit | A popular framework for implementing Spec-Driven Development. |
| Kiro | An AI-powered development environment with specification-driven workflows. |
| OpenSpec | A fast and highly configurable option for managing specifications and AI-assisted development. |

**Initial impression:** OpenSpec seems like a particularly interesting option because of its speed, flexibility, and configurable workflow.

Further experimentation is needed before making a final choice.

---

## 3. OpenSpec

OpenSpec is a framework designed to help developers structure AI-assisted software development around specifications.

Rather than immediately implementing a feature, we use a structured workflow to explore, propose, implement, and document changes.

### 3.1 Installation

Install OpenSpec globally using npm:

```bash
npm install -g @fission-ai/openspec@latest
```

### 3.2 Initial configuration

After installation:

1. Initialize OpenSpec in your project.
2. Select the AI development tools you want to use (e.g., Claude Code, Codex, etc.).
3. OpenSpec installs/configures the corresponding skills and instructions for your selected tools.
4. Review the generated project structure and configuration.

### 3.3 Important skills

The most important OpenSpec skills identified during the initial study are:

| Skill | Purpose |
|---|---|
| `openspec-explore` | Explore an idea, discuss possible implementations, ask questions, and clarify requirements. |
| `openspec-propose` | Create a structured proposal for a new feature or change. |
| `openspec-apply-change` | Implement a change based on its specification. |
| `openspec-archive-change` | Archive a completed change and incorporate its finalized documentation into the project specifications. |

#### openspec-explore

Used during the discovery and brainstorming phase.

Its purpose is to help transform an initial idea into something better defined.

Examples:
- Explore a feature idea.
- Identify possible implementation approaches.
- Ask questions about unclear requirements.
- Identify edge cases and potential problems.
- Discuss technical alternatives before making decisions.

This is particularly useful when the initial requirements are incomplete.

#### openspec-propose

Used to transform an idea into a structured change proposal.

The proposal should establish what will be changed and provide the necessary documentation to guide implementation.

#### openspec-apply-change

Used to execute the implementation described in the approved change proposal.

The AI agent uses the specification as its reference rather than relying exclusively on the conversation context.

#### openspec-archive-change

Used after completing a change.

It archives the completed change and updates the project's specifications where appropriate, helping maintain the single source of truth.

---

## 4. OpenSpec Configuration

OpenSpec provides a `config.yaml` file where project-level configuration and technical decisions can be documented.

This is useful for establishing conventions that AI agents should follow throughout development.

Examples of decisions worth documenting:

- Programming languages and frameworks.
- Architectural patterns.
- Coding conventions.
- Project structure.
- Testing strategies.
- Naming conventions.
- Infrastructure decisions.
- Technical constraints.

**Important:** These decisions should be documented centrally instead of repeatedly explained in individual AI conversations.

---

## 5. Initial Workflow

Based on the concepts studied so far, the development process can be represented as follows:

1. **Explore:** Understand the problem, discuss the idea, and clarify requirements.
2. **Propose:** Create a structured specification for the proposed change.
3. **Review:** Validate the requirements and technical decisions before implementation.
4. **Apply:** Implement the change using the specification as the reference.
5. **Verify:** Check whether the implementation satisfies the requirements.
6. **Archive:** Finalize the change and update the project's specifications.

The main idea is to separate thinking, planning, and implementation instead of mixing everything into a single AI conversation.

---

## 6. Topics to Investigate Further

- [ ] Understand the complete OpenSpec directory structure.
- [ ] Investigate the difference between project specifications and change proposals.
- [ ] Understand how OpenSpec manages requirements and technical designs.
- [ ] Investigate how `config.yaml` influences AI agent behavior.
- [ ] Understand how OpenSpec handles changes to existing specifications.
- [ ] Explore how to use OpenSpec with Codex.
- [ ] Compare OpenSpec with Spec Kit and Kiro.
- [ ] Build a small experimental project using the complete workflow.
- [ ] Test whether specifications remain consistent across independent AI sessions.
- [ ] Investigate how to validate implementations against specifications.

---

## 7. Main Takeaway

**Spec-Driven Development is about making specifications the foundation of AI-assisted software development.**

Instead of treating the AI conversation as the project's memory, we create persistent, structured documentation that guides development across multiple sessions.

This makes complex projects easier to manage, improves consistency, and reduces dependence on the AI's limited context window.

