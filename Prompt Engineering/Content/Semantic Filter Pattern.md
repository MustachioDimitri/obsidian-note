#### **Overview**

The **Semantic Filter Pattern** leverages large language models (LLMs) to analyze text and remove specific content based on its meaning. This pattern is highly valuable for processing text to remove sensitive or redundant information while preserving the overall context. Unlike simple keyword-based filters, the semantic filter operates on an understanding of the meaning behind the text, enabling nuanced and context-sensitive editing.

---

### **Key Elements of the Pattern**

1. **Filter Instructions:** Clearly state what to remove and why.
    - Example: "Remove all dates from this text while maintaining readability."
2. **Semantic Understanding:** Define removal rules that rely on understanding the meaning of the text rather than just patterns or keywords.
    - Example: "Remove any references that indicate the patient has diabetes."
3. **Rewrite if Necessary:** Specify whether the model should modify the text to address any gaps created by the removals.
    - Example: "Rewrite the text minimally to ensure grammatical accuracy."

---

### **Steps to Implement the Semantic Filter**

1. **Formulate a Prompt:**
    
    - Define the filtering task explicitly.
    - Specify the rules for removal and optional rewriting.
2. **Feed Input Text:**
    
    - Provide the raw text for the filter to process.
3. **Evaluate Output:**
    
    - Review the filtered text for accuracy and completeness.
4. **Refine if Needed:**
    
    - Adjust the prompt for clearer instructions or specific edge cases.

---

### **Examples**

#### **Example 1: Removing Dates**

**Prompt:**  
"Filter this information to remove all dates and rewrite the text as minimally as possible to fix any issues caused by the date removals."

**Input:**  
"Vanderbilt University was founded in 1873. It celebrated its 150th anniversary in 2023."

**Output:**  
"Vanderbilt University was founded in the 19th century. It celebrated its anniversary recently."

---

#### **Example 2: Masking Medical Information**

**Prompt:**  
"Filter the information below to remove any details that might indicate the patient has diabetes. First, explain what you will remove and why, then provide the filtered information."

**Input:**  
"The patient presents with increased thirst and fatigue. Medical history includes Type 2 Diabetes, managed with Metformin."

**Explanation:**

- **Increased thirst:** Common symptom of diabetes.
- **Type 2 Diabetes in medical history:** Directly discloses the condition.
- **Metformin:** Medication commonly associated with diabetes management.

**Output:**  
"The patient presents with fatigue. Medical history includes no significant findings. Current medications are not listed."

---

### **Use Cases**

1. **Privacy Filtering:**
    
    - Remove personally identifiable information (PII) or sensitive data from documents.
    - Example: "Filter out names, addresses, and phone numbers."
2. **Simplification:**
    
    - Reduce redundant or irrelevant information to simplify reports.
    - Example: "Filter to remove repeated statements in this email thread."
3. **Content Moderation:**
    
    - Remove inappropriate or sensitive topics from text submissions.
    - Example: "Filter text to remove offensive language."

---

### **Advantages**

- **Semantic Precision:** The filter relies on meaning, not just keywords, allowing for smarter processing.
- **Adaptability:** It can handle complex and nuanced tasks, such as detecting indirect references.
- **Rewrite Capability:** Ensures the filtered text remains coherent and meaningful.

---

### **Limitations**

1. **Imperfect Results:** Outputs may occasionally miss key elements or remove unintended parts.
2. **Lack of Consistency:** Results might vary slightly across different runs for the same input.
3. **Human Review Needed:** Particularly for critical tasks like privacy filtering, a human should validate the output.

---

### **Prompt Template**

Here’s a general-purpose prompt for applying the Semantic Filter Pattern:

**"Filter this text to remove [specific content] while preserving its overall meaning. Rewrite as minimally as possible to ensure readability."**

---

### **Best Practices**

1. **Be Explicit:** Clearly define the type of content to filter.
2. **Iterate Prompting:** Refine instructions based on observed outputs to improve accuracy.
3. **Combine with Other Tools:** Use additional validation or checks for critical tasks (e.g., privacy or compliance filtering).

The **Semantic Filter Pattern** is a robust method to manipulate and clean text, empowering workflows where meaning and precision are paramount.
# Format of the Semantic Filter Pattern
To use this pattern, your prompt should make the following fundamental contextual statements:

- Filter this information to remove X
    

You will need to replace "X" with an appropriate definition of what you want to remove, such as. "names and dates" or "costs greater than $100".

Examples:

- Filter this information to remove any personally identifying information or information that could potentially be used to re-identify the person.
    
- Filter this email to remove redundant information.