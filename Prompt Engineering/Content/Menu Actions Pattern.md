**Overview:**  
The Menu Actions Pattern is a framework for creating reusable, shareable, and structured prompts. It mimics software menus (like a file menu in a word processor) by defining actions you can repeatedly trigger during a conversation. This approach simplifies complex workflows by embedding a predefined set of actions into your prompts. It’s particularly useful for repetitive tasks, collaborative environments, and when standardizing best practices.

---

### **Key Elements of the Menu Actions Pattern**

1. **Action Definition:**
    
    - Clearly specify the **trigger format** (`Whenever I type: X`) and the **action** (`you will do Y`).
    - Optionally define additional actions (`Whenever I type Z, you will do Q`).
2. **Feedback Loop:**
    
    - At the end of each action, the system prompts you for the next action: _"What would you like to do next?"_
3. **Reusability:**
    
    - Designed for tasks you perform frequently, reducing cognitive load by not having to retype detailed prompts each time.
4. **Customizability:**
    
    - Actions can incorporate placeholders (`<TASK>`, `<ITEM>`) to make them flexible and adapt to different inputs.
5. **Collaboration and Knowledge Sharing:**
    
    - Standardized actions can be shared across teams, ensuring consistency in workflows.

---

### **Benefits**

- **Efficiency:** Allows for quick task execution without retyping or restructuring prompts.
- **Consistency:** Ensures uniform execution of repeated tasks.
- **Scalability:** Can be scaled for individual use or organizational collaboration.
- **Ease of Use:** Simplifies interactions by mimicking familiar interface designs like dropdown menus.

---

### **Building a Menu Actions System**

To implement the Menu Actions Pattern, follow these steps:

#### **Step 1: Define Actions**

Write out the menu options and their corresponding behavior. Use placeholders where flexibility is required.  
Example:

plaintext

Copy code

`Whenever I type "write <BULLET POINT> <NUMBER OF PARAGRAPHS>", you will write content for the specified bullet point in the outline, generating the given number of paragraphs.   Whenever I type "expand <BULLET POINT>", you will expand the specified bullet point in the outline, adding subpoints.   At the end, ask me for the next action.`

#### **Step 2: Test Actions**

Validate each action's response to ensure the outputs align with expectations.

#### **Step 3: Add a Feedback Loop**

Include a prompt to ask what action should come next, maintaining a smooth interaction flow:

plaintext

Copy code

`At the end, ask me: "What would you like to do next?"`

---

### **Examples of Usage**

#### **Example 1: Expanding Outlines and Writing Text**

Input:

plaintext

Copy code

`Whenever I type "write <BULLET POINT> <NUMBER OF PARAGRAPHS>", you will generate text for that outline point. Whenever I type "expand <BULLET POINT>", you will create subpoints for the outline item. At the end, ask me for the next action.`

Workflow:

1. **Expand Outline:**  
    Input: `expand 3.5.2`  
    Output: Generates subpoints under outline item 3.5.2.
    
2. **Generate Text:**  
    Input: `write 3.5.2 2`  
    Output: Writes two paragraphs of text based on outline point 3.5.2.
    
3. **Next Action Prompt:**  
    Output: _"What would you like to do next?"_
    

---

#### **Example 2: Grocery List Management**

Input:

plaintext

Copy code

`Whenever I type "add <FOOD>", you will add <FOOD> to my grocery list and update my estimated grocery bill.   Whenever I type "remove <FOOD>", you will remove <FOOD> from my grocery list.   Whenever I type "save", you will suggest cheaper alternatives to the items in my grocery list.   At the end, ask me for the next action.`

Workflow:

1. **Add Item:**  
    Input: `add apples`  
    Output: Adds apples to the grocery list and updates the bill.
    
2. **Suggest Savings:**  
    Input: `save`  
    Output: Lists cheaper alternatives for the items in the grocery list.
    
3. **Next Action Prompt:**  
    Output: _"What would you like to do next?"_
    

---

### **Best Practices**

1. **Start Simple:**
    
    - Begin with basic actions, then add complexity as needed.
2. **Use Clear Keywords:**
    
    - Choose intuitive action names (e.g., `write`, `expand`, `save`) to avoid confusion.
3. **Validate Outputs:**
    
    - Regularly test actions to ensure consistent behavior.
4. **Encourage Collaboration:**
    
    - Share well-documented menu action templates across teams or communities.
5. **Iterate as Needed:**
    
    - Adjust actions based on feedback or evolving requirements.

---

### **Advanced Applications**

- **Customer Support Portals:** Codify actions like retrieving account information, FAQs, or troubleshooting steps.
- **Knowledge Management:** Build a shared menu for accessing and expanding organizational documents.
- **Educational Tools:** Automate common educational tasks, like expanding notes or generating study guides.

---

**Summary:**  
The Menu Actions Pattern transforms prompt engineering into a structured, reusable, and collaborative process. By codifying actions into an intuitive menu-like structure, users can streamline workflows, maintain consistency, and enhance productivity.
# Format of the Menu Actions Pattern

To use this pattern, your prompt should make the following fundamental contextual statements:

- Whenever I type: X, you will do Y.
    
- (Optional, provide additional menu items) Whenever I type Z, you will do Q.
    
- At the end, you will ask me for the next action.
    

You will need to replace "X" with an appropriate pattern, such as "estimate <TASK DURATION>" or "add FOOD". You will then need to specify an action for the menu item to trigger, such as "add FOOD to my shopping list and update my estimated grocery bill".

Examples:

- Whenever I type: "add FOOD", you will add FOOD to my grocery list and update my estimated grocery bill. Whenever I type "remove FOOD", you will remove FOOD from my grocery list and update my estimated grocery bill. Whenever I type "save" you will list alternatives to my added FOOD to save money. At the end, you will ask me for the next action. Ask me for the first action.
    

Mark as completed

Like

Dislike

Report an issue