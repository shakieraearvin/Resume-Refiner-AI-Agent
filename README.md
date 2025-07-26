# Resume-Refiner-AI-Agent

## Overview

### AI Agent Flow diagram

<img width="1074" height="689" alt="Screenshot 2025-07-26 at 7 21 11 PM" src="https://github.com/user-attachments/assets/08323f43-c9ad-4139-a356-2d6fb7e44a26" />


### Building the Agent

#### What approach did you take to design your agent?

Initially, I assumed I would need a complex web of nodes to complete the Resume Refiner AI Agent. But once I reviewed the available n8n nodes and tools, I realized I could simplify the process by breaking it down into small, manageable steps. This allowed me to design a lean, functional workflow that focused only on what was essential: collecting user input, extracting the resume text, fetching the job posting, sending it to OpenAI, and emailing the suggestions. Focusing on clarity over complexity helped me troubleshoot more effectively and build a working product faster.

#### What challenges did you face in parsing, formatting, or integrating?

One of the most challenging parts of building this agent was formatting the JSON correctly, especially when working with the OpenAI response and referencing node outputs. At times, I was overcomplicating things by trying to handle too many moving pieces at once. I learned that simplifying the workflow and using consistent naming conventions made the logic easier to follow and debug. Once I focused on keeping the data structure clean and the node connections direct, everything started to click.

#### How did you ensure that the AI returned JSON reliably?

While building the workflow, I ran into several issues with expressions and field references, especially when trying to pull data from earlier nodes like the form submission or OpenAI output. What helped the most was using the expression tool in n8n. It gave instant feedback and showed the resolved value when the input was correct. This made it easier to catch typos, incorrect node names, or references to fields that didn’t exist yet. It also helped me better understand how to navigate JSON data structures inside the workflow.

### Troubleshooting

#### What issues did you encounter and how did you resolve them?

My biggest issue was getting the JSON references correct. It was a bit tricky at first, especially when trying to pull data from previous nodes like the resume file or the OpenAI response. What really helped was using the expression tool in n8n. It made the process much easier by showing exactly what each expression resolved to, which helped me catch mistakes and simplify the workflow.

### Optimization 

#### What might you improve or add in future iterations?

One area I would improve is the formatting of the email output. Right now, the email is functional, but the UI could be more visually appealing to the user. I would enhance the layout using better HTML styling, clearer section headings, and maybe even add a branded header or bullet formatting to make the suggestions easier to read. A more polished presentation would help the user feel more confident and engaged with the AI's feedback.


### Screenshots!

#### n8n full agent workflow.

<img width="1505" height="338" alt="Screenshot 2025-07-26 at 7 24 08 PM" src="https://github.com/user-attachments/assets/c35c5007-0174-46df-814d-06ef3f152039" />

#### Configuration of AI agent node.

<img width="2004" height="1233" alt="Screenshot 2025-07-26 at 7 35 11 PM" src="https://github.com/user-attachments/assets/1b2abbd0-22f1-49ff-bc83-7c275d907385" />


#### Configuration of trigger and email node.

<img width="2021" height="1254" alt="Screenshot 2025-07-26 at 7 36 02 PM" src="https://github.com/user-attachments/assets/0829c4b0-0e63-4673-a18e-2f036eeb7b76" />


#### Example of form input and output email.

<img width="586" height="663" alt="Screenshot 2025-07-26 at 7 38 59 PM" src="https://github.com/user-attachments/assets/55baafaa-5250-437d-8001-9aae9fac7113" />


<img width="1258" height="818" alt="Screenshot 2025-07-26 at 7 37 36 PM" src="https://github.com/user-attachments/assets/0f2998d5-4715-48af-8d36-a2ce5ae9d63c" />
