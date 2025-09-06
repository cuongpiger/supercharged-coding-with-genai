# Downsides of Coding with GenAI

<hr>

While Generative AI (GenAI) offers significant value and benefits for software engineering, the sources also highlight several **downsides and challenges** that developers and organizations must address. These limitations temper the overall value proposition of GenAI, requiring careful management and human oversight.

Here are the key downsides of coding with GenAI:

1.  **Accuracy and Reliability Issues (Bugs & Hallucinations):**

    - GenAI tools are "certainly not perfect". Early studies in 2022 showed GitHub Copilot's accuracy for correct code was "below 50%".
    - GenAI has been observed to produce "some of the worst fatal development mistakes". Examples include a data scientist accidentally exposing "secret tokens" by committing an environment file or a software developer crashing a microservice due to a file renaming error. This indicates that GenAI can "supercharge your weaknesses" alongside your strengths.
    - A well-documented problem with LLMs is their tendency to **"hallucinate or fabricate information"** when answers are not apparent, and these "hallucinations and other LLM issues do occur when GenAI is applied to software engineering". This directly impacts the trustworthiness of generated code and explanations.
    - Specific examples of failure include an OpenAI bug fixer prompt that did not resolve all compilation, reproducibility, logical scoping, or error handling issues, and even "introduced a new issue related to casting the input to an integer" without proper error handling.
    - GenAI-generated unit tests can be "unnecessary or incorrect", with one example showing ChatGPT producing "one incorrect test out of seven". A 2024 IEEE study found that "unit tests written by humans have fewer errors than unit tests by GenAI". This means generated tests may "lack full coverage and may be incorrect".

2.  **Code Quality and Maintainability Degradation:**

    - If "prompted incorrectly," GenAI can **"degrade code quality"**. This often manifests as merging monitoring tasks (logging, input validation, counters) with the function's core functionality, thereby **"violating the single responsibility principle"**.
    - GenAI tools may suggest "using print statements instead of proper logging" or handling input validation directly within functions, leading to "cluttered, combining these elements with core functionality". This makes functions "longer and more complex" and "less readable".
    - Docstring generation, while helpful, can sometimes produce "exceedingly long lines or different formats" and include "unclear" sections, failing to adhere to specific style guides.

3.  **Security and Data Privacy Risks:**

    - The incident where a data scientist exposed "secret tokens" via a poorly crafted prompt and `git add .` highlights a critical **security risk related to data leakage**.
    - While GitHub Copilot encrypts data and deletes context without storing it for training, the mere act of sending parts of the current file and other open files to a remote server for context raises **inherent security concerns**.

4.  **Cognitive Impact and Skill Erosion for Developers:**

    - Developers have concerns that relying on GenAI tools might "turn them into less capable developers" or cause them to "lose their programming edge or familiarity with the functions".
    - Research suggests that AI tools could "decrease our critical thinking capability through a process known as cognitive off-loading". For instance, developers might take longer to remember exact syntax if the internet is down, indicating a potential over-reliance.

5.  **Training Data Limitations and Model Mastery Gaps:**

    - GenAI performs well for "problems that are widely documented, such as the Fibonacci sequence calculation". However, it has "far more difficulty solving more obscure coding tasks where there is far less training data". A slight change to a common problem (e.g., LeetCode's Two Sum with Python Threads) can lead to "unpredictable" solutions.
    - The "model’s mastery" of a topic can be reduced if tasks are combined (e.g., explaining and fixing bugs in one prompt), as this "may be less common" in its training data.
    - GenAI "often fails without such expansive sets of examples," especially for "domain-specific languages" or new technologies like "databases, cybersecurity, quantum computing".

6.  **Unpredictability and Inconsistency:**

    - GenAI applications "rarely output deterministic results," meaning "responses for similar prompts may differ due to prompt construction, user customization, and randomness". This makes it challenging to achieve consistent results.
    - Even when generating docstrings, Copilot can produce "several variations," sometimes with "exceedingly long lines or different formats".

7.  **Legal and Ethical Concerns (Copyright, Responsibility):**

    - Some GenAI suggestions "may be subject to copyright protection". The "copyright issue of software" is a relatively new problem, and "GenAI could duplicate copyrighted code".
    - The "risks, legal responsibilities, and ethical considerations will need to address responsibilities and safeguards for software," particularly in heavily regulated industries. Humans remain "ultimately responsible for the code that is produced".

8.  **Job Displacement and Shifting Developer Landscape:**

    - The sources speculate that the increased efficiency of GenAI "will shift toward senior developers, and more junior developers may be displaced by the GenAI tools". This is because GenAI efficiencies "clearly overlap the skillsets of the junior developers," which tend to focus more on writing code, tests, and documentation.

9.  **Necessity of Human Oversight and Verification:**

    - Despite GenAI's capabilities, "you should verify the output you get". The "variability of the unit tests with correct and incorrect responses means that checking them must be part of the verification process".
    - It is "strongly recommended to use GenAI to save time, but to use human intelligence to verify that they are correct. At the present time, trust but verify is the best approach". This means GenAI does not eliminate the need for careful human review.

10. **Challenges in Full Value Realization (Integration, Training):**
    - One study reported "much more modest" productivity gains (3.99%) compared to others, partially attributed to not characterizing "the training, familiarity, or integration of GenAI into their workflows". This indicates that simply having access to GenAI does not automatically translate to maximum value without proper training and integration.
    - Achieving desired outputs often requires effort in "prompt engineering," which includes "multiple rounds to achieve the desired output". Fine-tuning models, an alternative to prompting, "requires more training examples than few-shot learning" and significant "time and effort".

In the larger context of GenAI for software engineering value, these downsides highlight that while GenAI offers unprecedented speed and automation, its value is not without complexities. The perceived "bargain" of GenAI tools must be weighed against the **hidden costs** of verification, refactoring poor-quality output, managing security risks, and investing in advanced prompt engineering or fine-tuning to mitigate these issues. The ideal scenario, as suggested by the sources, is to leverage GenAI for rapid assistance while maintaining a critical and informed human perspective to ensure quality, security, and maintainability.
