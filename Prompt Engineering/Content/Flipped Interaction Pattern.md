The _flipped interaction pattern_ is a prompt technique that allows a large language model (LLM) to take the lead in solving a problem by asking _you_ the questions, guiding you toward a solution step-by-step. This pattern is useful when you’re not entirely sure of the steps needed to reach a goal, but you know what information you can provide. Rather than you asking the LLM questions, this pattern "flips" the interaction: the model does the questioning, and you provide the answers. This way, the model gathers information until it can deliver the outcome you need.

### Key Elements of the Flipped Interaction Pattern

1. **Flipping the Roles**:
    
    - Instead of you asking questions and the model responding, you ask the model to _ask you questions_. This can be especially useful when you lack detailed knowledge about the topic but have specific information to share that can help guide the model.
2. **Establishing a Goal**:
    
    - You start by specifying what you want to achieve. This can be as simple as: “Ask me questions about fitness goals until you have enough information to create a strength training regimen for me.”
    - The model then understands its purpose and can ask relevant, targeted questions to reach that end goal.
3. **One Question at a Time**:
    
    - To make the interaction manageable, you can include “Ask me the first question” in your prompt. This often encourages the model to ask questions one at a time, creating a natural, conversational flow that builds toward a more accurate, personalized outcome.

### Examples and Explanation

#### Example 1: Developing a Fitness Routine

Let’s say you want a custom strength training regimen but aren’t sure what information the model needs. You could use the flipped interaction pattern like this:

- **Prompt**: “Ask me questions about my fitness goals until you have enough information to suggest a strength training regimen. When you have enough information, show me the training plan. Ask me the first question.”

The model begins by asking, “What are your specific fitness goals? Are you looking to build muscle, increase strength, endurance, or achieve a particular goal?”  
You answer with specifics, such as, “I want to build explosive power and prevent knee issues related to mountain biking.”

The model then continues with relevant follow-up questions, like asking about past injuries, available workout equipment, and how much time you can dedicate each week. Once it has enough details, it generates a tailored strength training regimen, integrating your answers into a specific plan for explosive power while addressing knee health.

#### Example 2: Diagnosing an Issue with Customer Support

Consider a scenario in customer service where an agent or an AI system might need more information to diagnose a problem with a product.

- **Prompt**: “Ask me questions to diagnose an issue with my smartphone until you can suggest a solution. Start with the first question.”

The model could start with basic troubleshooting questions, such as, “Is your smartphone turning on? Are you experiencing issues with the screen or battery?” Based on your responses, it will ask further questions to isolate the problem—eventually offering a tailored solution like adjusting settings, replacing the battery, or other potential fixes.

#### Example 3: Learning About a Subject Through Quizzing

If you want to test your knowledge on a subject, the model can be guided to quiz you:

- **Prompt**: “Ask me questions to quiz my knowledge on basic biology concepts. Ask one question at a time and let me know if my answers are correct.”

The model might ask, “What is the powerhouse of the cell?” and based on your response, it will provide feedback and move to the next question, adapting its questions to reinforce key concepts or test areas where you might need more practice.

### Why This Works

The flipped interaction pattern leverages the model's training and pattern recognition to drive the conversation towards a structured and well-informed result. Here’s why it’s effective:

1. **Access to Implied Knowledge**:
    
    - The model’s training data includes patterns of language and commonly asked questions in various fields, such as fitness, diagnostics, or customer support. It "knows" which questions to ask, helping you achieve a goal even if you’re unfamiliar with the typical process.
2. **Minimizes Uncertainty and Guesswork**:
    
    - When you don’t know what questions need to be asked to get a clear answer, the model can “think ahead” based on patterns it has seen, sparing you the guesswork.
3. **Adaptability Across Scenarios**:
    
    - This pattern is versatile, effective for creating training plans, troubleshooting problems, guiding educational quizzes, and more. Essentially, anytime you need an informed guide to lead you toward a goal, the flipped interaction pattern is valuable.

### Practical Applications of the Flipped Interaction Pattern

This pattern can be useful in various fields:

- **Education**: Tutoring a student by asking sequential questions on a topic, gauging comprehension before explaining further.
- **Health and Fitness Coaching**: Creating personalized plans based on health goals and constraints, with the model asking questions about injuries, equipment access, and time commitment.
- **Product Troubleshooting**: Helping users troubleshoot complex issues by asking detailed diagnostic questions.
- **Self-Discovery and Coaching**: Asking reflective questions to guide a user through problem-solving, decision-making, or exploring a new topic in-depth.

With the flipped interaction pattern, you can let the LLM lead the way in obtaining the details it needs for a clear and precise output, offering a guided path toward your goal without needing to know each step ahead of time.