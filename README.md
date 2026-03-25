# AI Interview Prep Assistant (LangChain RAG)

A lightweight Retrieval-Augmented Generation (RAG) app that helps you prepare grounded, professional interview answers using **your resume + job description + company notes**.

**What this notebook demonstrates:**
- Document ingestion (PDF + TXT)
- Chunking + embeddings
- FAISS vector search
- Context-grounded answers with source attribution
- Clean, production-style code structure
- Gradio for evaluation  interactive UI

**How it works:**
1. Load documents from `/data`
  a. FIRST: Create a /data directory and upload your 3 - TXT files - Resume, Job Description, Company notes your interviewing
2. Using an OPENAI_API_KEY of your choice
3. Split → embed → store in FAISS
4. Retrieve relevant chunks
5. LLM answers using **only** the retrieved context (no hallucinations)
6. Gradio UI to display LLM-as-Judge results (WebInterface to Prompt your asks !!) 

Sample Prompts and Output 

🔹 Question: Why am I a strong fit for this role?
Answer:
You are a strong fit for this role due to your proactive approach to challenges, strong leadership qualities, and commitment to driving impactful results.

1. **Proactive Problem-Solving**: Your tendency to "dive in to fight the fire" resonates with the company's culture of facing challenges head-on and solving problems with grit and resilience.

2. **Ownership and Execution**: As someone who operates with maximum agency, you exemplify the qualities of a "benevolent dictator" in your domain, driving ideas with conviction and biasing toward action. This aligns with the expectation that each team member is responsible for ultimate results.

3. **Commitment to Success**: Your willingness to "run to the roar" reflects a deep care for both company and customer success, matching the organization's drive to create meaningful impact in a fast-moving environment.

**Suggestion**: Highlight specific achievements from your past experiences that illustrate these qualities to further strengthen your fit for the role.

🔹 Question: Give me a 60-second pitch for this company
Answer:
We are a company committed to building something great in a fast-paced environment, actively embracing challenges with grit and resilience. Our culture thrives on problem-solving, allowing us to dive headfirst into issues and emerge stronger, together. 

1. Our unwavering dedication to excellence is evident as we reject mediocrity and encourage rapid iterations to enhance our offerings, ensuring we remain at the forefront of innovation.
   
2. We foster a culture of open communication where 'hot takes' are not only welcomed but encouraged. This approach helps challenge the status quo and facilitates the quick identification and resolution of problems, driving continuous improvement.

3. Backed by industry recognition, our strategic focus includes cutting-edge tools like LangSmith, enabling developers to quickly debug, evaluate, and deploy solutions effectively.

I suggest emphasizing our commitment to agility and collaboration in your discussions, as these are key differentiators in our dynamic industry landscape.

🔹 Question: What gaps should I address before interviewing?
Answer:
**Direct Answer:**  
To enhance your interview readiness, focus on refining your storytelling for leadership achievements and quantifying your impact across various roles.

**Supporting Points:**  
1. **Leadership Experience:** Highlight specific instances where you aligned cross-functional teams to achieve business goals, providing clear examples of how your strategic direction contributed to successful outcomes.  
2. **Quantifiable Outcomes:** Prepare to articulate your achievements in terms of numbers, such as your experience with exceeding quotas (105–198% attainment) and how your initiatives led to revenue growth or operational efficiencies.  
3. **Ethical Leadership:** Emphasize your accomplishments in ethical leadership, which is increasingly crucial in today’s business landscape—this can differentiate you from other candidates.

**Suggestion:** Consider practicing common interview questions that focus on behavioral and situational responses to effectively convey your leadership style and the impact of your contributions.


This includes an LLM-as-Judge evaluator with clear scores and explanation on 3 key areas: Groundedness, Relevance, and Professionalism. 
![EvalLLMJudge](EvalLLLasJudge.png)
