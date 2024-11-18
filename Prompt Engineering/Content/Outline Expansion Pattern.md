#### **1. Combining Patterns for Sophisticated Prompt Design**

When solving complex problems, instead of focusing on a single pattern, consider **combining multiple prompt patterns**. Each pattern addresses a specific aspect of a problem, and together they provide a comprehensive solution.

- **Key Concept**: Break down the problem into smaller components and apply appropriate patterns to each. The remaining unaddressed components should ideally be minimal.

---

##### **1.1 Importance of Combining Patterns**

- **Efficiency**: Combining patterns reduces the need for inventing new solutions from scratch.
- **Flexibility**: Allows tackling diverse tasks by leveraging known frameworks.
- **Modularity**: Patterns act like building blocks, simplifying complex prompt design.

##### **1.2 Examples of Pattern Combinations**

- **Ask for Input + Alternative Approaches**:
    - Use "ask for input" to ensure the AI doesn't proceed without user direction.
    - Combine it with "alternative approaches" to explore various strategies for solving a problem.
- **Persona Pattern + Ask for Input + Tail Generation**:
    - Define a specific role for the model (persona pattern).
    - Use "ask for input" to maintain control.
    - Add "tail generation" to keep the flow organized (e.g., asking for the next input).

---

##### **1.3 Challenges in Combining Patterns**

- **Placement Matters**: Certain elements, like "ask for input," must appear in specific places (e.g., at the end of the prompt).
- **Nuance in Integration**: While some combinations are straightforward, others require careful thought to ensure clarity and functionality.

---

#### **2. Managing Large-Scale Outputs with Outline Expansion**

Large language models have limits on:

1. **Input Size**: Maximum content that can be processed in one go.
2. **Output Length**: Maximum content that can be generated in a single response.

To address this, adopt **outline-based approaches** for breaking down tasks into manageable components.

---

##### **2.1 The Outline Expansion Pattern**

This pattern helps create structured, expandable outlines that serve as a roadmap for generating detailed outputs.

- **Core Instruction**:
    - Ask the model to generate an outline for a topic.
    - After the outline is ready, focus on expanding specific bullet points.
    - Use **tail generation** to ensure the model asks what to expand next.

##### **2.2 Steps for Using Outline Expansion**

1. **Define the Task**: Clearly describe what the outline is about.
    - Example: _"Create an outline for writing effective prompts for ChatGPT."_
2. **Generate an Initial Outline**: Request a top-level structure.
    - Example Output:
        - 1. Introduction to ChatGPT
        - 2. Importance of Prompts
        - 3. Tips for Writing Effective Prompts
        - ...
3. **Select Points to Expand**: Specify which part of the outline to develop.
    - Example Request: _"Expand on point 3: Tips for Writing Effective Prompts."_
4. **Iterative Detailing**: Drill down into subsections for finer granularity.
    - Example Expansion:
        - 3. Tips for Writing Effective Prompts:
            - 3.1 Use Specific Instructions
            - 3.2 Experiment with Different Styles
            - ...
5. **Reintegrate Context**: As the outline grows, reintroduce relevant parts of the structure to maintain cohesion.

---

##### **2.3 Benefits of Outline Expansion**

- **Scalability**: Supports breaking large tasks into smaller, manageable chunks.
- **Clarity**: Ensures all parts fit together logically.
- **Reusability**: Individual sections can be revisited or expanded further.
- **Flexibility**: Allows non-linear development (e.g., jumping between sections).

---

##### **2.4 Challenges and Solutions**

- **Context Retention**: AI might "forget" earlier parts in long conversations.
    - **Solution**: Copy and paste relevant parts of the outline back into the prompt.
- **Consistency Across Sections**: Ensure all pieces align in tone and content.
    - **Solution**: Provide references to other outline parts during generation.

---

#### **3. Practical Application Example**

**Task**: Create an outline for a guide on "Effective Team Collaboration."

**Prompt**: _Act as an outline expander. Generate a bullet point outline for the topic I provide. Afterward, ask me which bullet point to expand. For each bullet point, generate a more detailed sub-outline. At the end of each response, ask what to expand next. Start by asking me for the topic._

**Output**:

- "Sure, what is the topic you'd like me to outline?"

---

#### **4. Key Takeaways**

1. **Combine Patterns Thoughtfully**: Address different facets of a problem by using complementary patterns.
2. **Leverage Outline Structures**:
    - Break down large tasks into outlines.
    - Expand incrementally for deeper detail.
3. **Iterate and Refine**: Continuously provide context to ensure consistency and quality across all sections.

This structured approach not only simplifies complex tasks but also ensures cohesive, high-quality outputs from large language models.
# Format of the Outline Expansion Pattern

To use this pattern, your prompt should make the following fundamental contextual statements:

- Act as an outline expander.
    
- Generate a bullet point outline based on the input that I give you and then ask me for which bullet point you should expand on.
    
- Create a new outline for the bullet point that I select.
    
- At the end, ask me for what bullet point to expand next.
    
- Ask me for what to outline.
    

Examples:

- Act as an outline expander. Generate a bullet point outline based on the input that I give you and then ask me for which bullet point you should expand on. Each bullet can have at most 3-5 sub bullets. The bullets should be numbered using the pattern [A-Z].[i-v].[* through ****]. Create a new outline for the bullet point that I select. At the end, ask me for what bullet point to expand next. Ask me for what to outline.