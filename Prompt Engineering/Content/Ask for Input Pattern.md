#### **Overview**

The "Ask for Input" pattern is a method used to guide large language models (LLMs) to focus on following user-defined rules while avoiding unnecessary or premature responses. This approach is particularly useful when working with flipped interactions or scenarios where LLMs might otherwise generate overly verbose or irrelevant output.

---

### **Key Concepts**

1. **Programming LLMs with Rules:**
    
    - In prompt engineering, we often define rules that LLMs must follow.
    - These rules act as a "program" for the LLM, guiding how it processes and responds to tasks.
2. **Challenge of Overgeneration:**
    
    - Without guidance, LLMs may immediately generate output based on their interpretation of the rules.
    - Example issue: If asked to provide alternative approaches for a task without specific input, the LLM might invent a task and generate unnecessary content.
3. **Solution – The "Ask for Input" Pattern:**
    
    - At the end of the prompt, explicitly instruct the LLM to **pause** and **ask for the user's input** before proceeding.
    - This ensures that the model does not assume or preempt the user's needs.

---

### **How the Pattern Works**

1. **Describe the Rules:**
    
    - Provide the LLM with clear, detailed instructions or rules it should follow.
2. **End with an Explicit Directive:**
    
    - After outlining the rules, conclude the prompt with a statement like:
        - **“Ask me for the first [input].”**
    - Replace `[input]` with the relevant context, such as:
        - "task," "question," "idea," "goal," or "thing to translate."
3. **Result:**
    
    - The LLM will acknowledge the rules and wait for user input before generating any further content.

---

### **Why This Works**

- **Stops Premature Output:** The model is cued to stop at the directive rather than responding to the rules immediately.
- **User-Driven Interaction:** The user maintains control, enabling more focused and relevant interactions.
- **Consistency and Clarity:** Helps avoid confusion or clutter in the conversation.

---

### **Examples**

#### **Without the Pattern:**

**Prompt:**  
_"Whenever I ask you to write a prompt for me to accomplish a task, list the task, provide alternative approaches, and write a prompt for each approach."_

**Model's Response:**  
_"Certainly. Here are three alternative approaches for the task of organizing a cluttered desk..."_

**Problem:**

- The model invents a task ("organizing a cluttered desk") without user input.
- The response is verbose and irrelevant.

---

#### **With the Pattern:**

**Prompt:**  
_"Whenever I ask you to write a prompt for me to accomplish a task, list the task, provide alternative approaches, and write a prompt for each approach. Ask me for the first task."_

**Model's Response:**  
_"Certainly. Let's begin. What is the first task you would like me to create alternative approaches and prompts for?"_

**Solution:**

- The model stops and waits for user input, enabling a focused and relevant interaction.

---

### **Practical Applications**

#### **Example 1: Summarizing Emails**

**Prompt:**  
_"From now on, I am going to cut/paste email chains into our conversation. You will summarize each person's points as bullet points. At the end, list any open questions or action items directed at me. My name is Jill Smith. Ask me for the first email chain."_

**Response:**  
_"Understood. Please provide the first email chain for summarization."_

---

#### **Example 2: Creative Translation**

**Prompt:**  
_"Translate anything I write into a dog's reactions using sounds and actions. Ask me for the first thing to translate."_

**Response:**  
_"Got it! What is the first thing you'd like me to translate into a dog's reactions?"_

---

### **Tips for Using the Pattern**

1. **Be Specific:**
    
    - Clearly outline what the model should do.
    - Ensure the directive at the end matches your intended interaction.
2. **Use Natural Language:**
    
    - Make instructions conversational and intuitive to improve model understanding.
3. **Adapt for Context:**
    
    - Customize the "[input]" type based on the task (e.g., "task," "idea," "story").
4. **Expect Variability:**
    
    - LLMs are stochastic; while this pattern is reliable, occasional deviations may occur.

---

### **Conclusion**

The "Ask for Input" pattern is a powerful prompt engineering technique to enhance control, focus, and efficiency when working with large language models. By explicitly instructing the model to await user input, we can streamline interactions, reduce irrelevant content, and create a more consistent conversational flow.