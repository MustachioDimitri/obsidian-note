The **Template Pattern** is an effective strategy for guiding a large language model (LLM) like ChatGPT to generate outputs that adhere precisely to your desired format. By creating a structured template with specific placeholders, you can ensure that the model fills in the content according to the layout and rules you’ve specified, similar to how you might instruct an assistant to use a form letter template with designated fields. Here’s a breakdown of how to apply this pattern:

### Template Pattern Structure

1. **Define a Template Structure**:
    
    - Begin by informing the model that it will use a specific template.
    - Capitalize placeholder words within the template to distinguish them from fixed elements.
    - Specify that it should preserve the formatting and fill in only the placeholders with generated content.
2. **Create a Template Example**:
    
    - Use Markdown or similar formatting guides, as models like ChatGPT render outputs in Markdown for bold, italics, headings, etc.
    - For instance, you might set up:
        
        plaintext
        
        Copy code
        
        `***Question***: QUESTION ***Answer***: ANSWER`
        
    - In this setup:
        - `***Question***` and `***Answer***` are structural text that will remain.
        - `QUESTION` and `ANSWER` (capitalized to denote placeholders) will be filled with generated content.
3. **Provide Clear Instructions for the Template**:
    
    - Explain any special formatting requirements, like using headings or bullet points.
    - Clarify if the placeholders should follow any specific rules, such as `QUESTION` containing open-ended queries or `ANSWER` being concise.

### Example: Generating Q&A from Text

Suppose you want to generate questions and answers from a text about Paleo-Indians. You’d:

1. Specify the template:
    
    plaintext
    
    Copy code
    
    `I'm going to give you a template for your output. Capitalized words are my placeholders. Please fill in placeholders with your output, preserving my formatting. My template is:  ***Question***: QUESTION ***Answer***: ANSWER`
    
2. Give content (e.g., a passage on Paleo-Indians) and ask for 20 question-answer pairs:
    
    plaintext
    
    Copy code
    
    `Use the information below to create 20 questions with answers using my template.`
    
3. The LLM will then fill in each `QUESTION` and `ANSWER` placeholder based on the content provided, following the specified format.

### Example: Creating Summaries for Individuals

Another scenario is summarizing biographies:

1. Provide a detailed template with constraints:
    
    plaintext
    
    Copy code
    
    `I'm going to give you a template. Capitalized words are placeholders. Fill in the template according to my rules.  ### Bio: NAME **Executive Summary**: A one-sentence summary of the person's role. **Full Description**: A one-paragraph summary.`
    
2. Feed in a passage with names and descriptions, and specify the number of profiles you want.
3. The LLM will output structured profiles with summaries meeting the sentence/paragraph constraints.

### Key Benefits of the Template Pattern

- **Precise Control**: Directs the model’s output structure.
- **Placeholder Flexibility**: Allows placeholders to contain complex instructions (e.g., summarizing text within a sentence or paragraph constraint).
- **Sophisticated Matching**: Enables the model to recognize and organize information meaningfully (like extracting names or roles).

Using the Template Pattern, you can achieve a high level of consistency and relevancy in responses, perfect for structured documents, question generation, content summaries, and more.