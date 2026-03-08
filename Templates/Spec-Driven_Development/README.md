# Practice 1: Spec-Driven Development (The Architect Paradigm)

## Overview
Spec-driven development is the most robust practice for building complex, professional-grade software with agents. It shifts the developer's role from "coder" to "architect," using high-reasoning models to plan before execution.

## Core Mechanism
1. **Requirement Detailing:** Meticulously define all requirements before generating any code.
2. **Technical Blueprint:** Use a high-reasoning model (e.g., Gemini 3 Pro) to generate an `architecture.md` file.
   - Database schemas
   - API endpoints
   - Technical constraints
   - Security requirements
3. **Sequential Implementation:** The agent follows the blueprint to implement each component.

## Efficiency Gains
- Prevents "bulldozing" (random implementation attempts followed by failure and deletion).
- Ensures high accuracy on the first attempt.
- Creates a maintainable and well-documented codebase.

## Template Steps

### Step 1: Research & Definition
Define the core goal and constraints.
- Goal: [Describe the primary objective]
- Constraints: [List tech stack, performance requirements, etc.]

### Step 2: Architecture Spec Generation
Prompt the agent to create `architecture.md`:
> "Act as a Senior Software Architect. Based on the following requirements: [Insert Requirements], generate a detailed `architecture.md` including database schemas, API specs, and a modular component breakdown. Do not write implementation code yet."

### Step 3: Review & Refine
Human review of the `architecture.md` file. Adjust until it meets the standard.

### Step 4: Component Implementation
Dispatch agents to implement specific modules identified in the spec.
> "Follow the `architecture.md` to implement the [Module Name]. Ensure it complies with the defined API and data structures."

## Best Practices
- Use `architecture.md` as the primary source of truth.
- Update the spec if requirements change mid-development.
- Mandatory checkpoints after each major component is built.
