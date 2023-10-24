Remark: *This serves as a provisional storage location for the materials utilized in developing the initial iteration of the AuCALME framework. Since the project is currently in a research and experimentation stage, we plan to make the source code available once we have achieved a stable and deployable version of the framework.*

# AuCALME Report

## Abstract:

"AuCALME" which stands for "Autonomous Collaborative Agents for Learning Methods Exploration," is a framework designed to automate the machine learning model development process by harnessing the cognitive capabilities of Large Language Models (LLMs). This innovative framework consists of specialized generative agents, each assigned to distinct facets of model development, employing predefined workflows. These agents interact with LLMs, generating tailored prompts and structuring responses for future use. The research explores the potential of Autonomous Agents, addressing challenges in handling complex queries and extended reasoning tasks, focusing on machine learning tasks ranging from data analysis to hyperparameter tuning.

The framework is evaluated across various machine learning tasks, showcasing its efficacy in managing diverse datasets, selecting appropriate learning methods, and enhancing model performance. It highlights the critical role of the quality and scale of the employed LLM, motivating further research to assess task-specific fine-tuned LLMs and the incorporation of verification agents to ensure task accuracy.

## Global Architecture:

The framework consists of virtual agents working collaboratively to solve a ML related problem. Each agent has its environment, which can include a coding environment, a plan, and an ensemble of shared files between it and other agents.

![Data Analysis(2)](https://github.com/MassixXx/AuCALME-temp/assets/88004644/5afdcf6d-5f6a-4eef-b369-d1de8a152275)



Here is the general pipeline that the system follows:
![Generate the data analysis plan(4)](https://github.com/MassixXx/AuCALME-temp/assets/88004644/c6855125-ab09-418b-abaf-08e986c5b0fa)



## Agents:

- **Data Analyst:** The primary responsibility of the Data Analyst is to extract pertinent information from the dataset to facilitate problem resolution. This involves formulating a systematic plan of action and subsequently sequentially executing tasks. At each step, the Data Analyst utilizes the outputs from preceding tasks to guide their exploration, thereby enhancing orientation and minimizing code errors.



![Generate the data analysis plan](https://github.com/MassixXx/AuCALME-temp/assets/88004644/09762d6d-c404-4cc7-b351-428e563788dc)



- **Data Engineer:** The role of the Data Engineer centers on implementing recommended preprocessing techniques on the dataset. This may encompass applying multiple preprocessing methods simultaneously or a selective subset thereof. Subsequently, the modified dataset is returned to the Data Analyst for further analysis.


![Generate the data analysis plan(1)](https://github.com/MassixXx/AuCALME-temp/assets/88004644/6418462c-a5ce-44b1-b086-7e7c09a3f1f3)


- **ML Specialist:** Positioned as the decision-maker in this framework, the ML Specialist is tasked with recommending the most suitable methodology based on the dataset's characteristics and the nature of the problem at hand. Additionally, the ML Specialist bears the responsibility of proposing enhancements grounded in the outcomes of experimental endeavors.


![Generate the data analysis plan(2)](https://github.com/MassixXx/AuCALME-temp/assets/88004644/6ab06628-b01b-4837-8df2-516adfb736cd)


- **ML Engineer:** The ML Engineer assumes the responsibility of translating the recommendations put forth by the ML Specialist into tangible code. This includes the development of the model, encompassing both the training and evaluation phases.


![Generate the data analysis plan(3)](https://github.com/MassixXx/AuCALME-temp/assets/88004644/b2d87dbf-2fe6-4360-a068-9b18f886b95a)


- **Coding Environment:** The Coding Environment serves as the platform through which coding agents execute their code and retrieve output. This output is essential for error handling and the retrieval of valuable information.


![Write code that satisfies the request(1)](https://github.com/MassixXx/AuCALME-temp/assets/88004644/1dd7b454-36a6-465d-98f8-0e46adc7bf43)


**Prompt Chaining system:**

For each task, the virtual agent interacts with the LLM with a set of predefined prompt templates filled with the information generated in the files by itself or the other agents.


![Ajouter un titre(2)](https://github.com/MassixXx/AuCALME-temp/assets/88004644/eed29708-345f-4c7b-8a21-2111c0ff7c20)


## Experiments:

1. **Binary classification on the titanic dataset:**

**Results:**

![Screenshot from 2023-10-18 17-55-16](https://github.com/MassixXx/AuCALME-temp/assets/88004644/36087267-1832-4d96-81ae-ad8be6d52839)


2. **Time series prediction on the traffic dataset:**

**Results:**

![Screenshot from 2023-10-18 17-56-17](https://github.com/MassixXx/AuCALME-temp/assets/88004644/91d2cfa1-b3f3-4c58-b3f3-58087fc66db6)


3. **Named Entity Recognition on the COVID19 dataset:**

**Results:**


![Screenshot from 2023-10-18 17-58-00](https://github.com/MassixXx/AuCALME-temp/assets/88004644/7b7221f5-04ba-4bb5-a066-f6e8ad7a79cc)


4. **Anonymous Curriculum Vitae summarizing using transformers:**

**Results:**

- "_SALES ASSOC\<sensitive\>TEOPLE: Experienced Manager at \<sensitive\> with excellent client and project management skills Actionoriented with strong ability tocommunicate effectively with technology executive and business audiences. Demonstrated the ability to complete tasks accurately despite interruptions and competing demands."_
- "_HR \<sensitive\>Specialist with over 9 years in recruitment and federal_

_employment processes. An energetic innovative out the box thinker with_

_excellent analytical organizational and project management skills. I rely on_

_excellent interpersonal skills outstanding customer service and a solid expertise in_

_human resources management. I possess an extensive background in HR_

_recruitment and staffing affairs."_

- "_\<sensitive\> AND \<sensitive\> MANAGER executive profile. Resultsdriven efficiencyconscious with extensive experience including financial management. Organizational development business development and team building within diverse industries. Skilled in planning coordinating and executing strategic business and financial programs with track record of improving operational stability efficiency and profitability._

## Conclusion:

Our framework has demonstrated significant efficacy in autonomously managing a machine learning development project. It excels in various aspects, such as handling datasets of different types and formats, conducting thorough analyses to select suitable learning methods, and exploring alternative approaches to enhance model performance.

It is worth noting that the quality and performance of our system are notably influenced by the quality and scale of the language model (LLM) employed. In our forthcoming research, we intend to evaluate our framework using smaller, ideally task-specific fine-tuned LLMs. Furthermore, we have investigated the concept of incorporating a verification agent to ensure task accomplishment and mitigate hallucinations. This exploration has yielded promising results and will be further investigated in our future research endeavors.

## Future works:
- Experience the framework's efficiency using different Large Language Models of different sizes fine-tuned on different datasets.
- Explore the ability to work with a diverse population of LLMs where each agent has its own fine-tuned task-specific version of LLM.
- Assess the system on a diverse set of problems on various datasets.
- Explore the ability of such a system to iteratively design the best model architecture (LLM-based Neural architecture search).
- Assess the system on data generation tasks (its ability to adapt a set of data to a particular problem, data augmentation,...).
- Explore the potential of such a system in Reinforcement Learning problems.
