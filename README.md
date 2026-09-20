Here , basically i exercised my agentic ai knowledge. Implemented it using Crew AI. Created A full stack website which can create website of you , you just have to give it some instruction.

Difficuties Faced:
1. Main problem was i used openai/gpt-oss-20b from Groq. It has a token limit of 8000/minute.  
   Everytime it was crossing the token limit as it was through a lot of agents Guardrail Agent, Prompt Enhancer agent, HTML-CSS-JS writing agent, 
   UI Improving agent, readme agent --- so overall it was taking hella lot of token, as this HTML blah blah agent was passing the whole code everytime
   to improve the UI...

   so, Now Solution --
   I strictly hardcoded a maximum number of tokens allowed and while creating instance of model. So it kinda reduced the number of tokens using,
   but again it was showing tokens exceeded like SERIOUSLY?? 

   Now i had one more weapon added delays in between sequential processes, added exponential-backoff retries for TPM errors ( like retry again after 30s)
