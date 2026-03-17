# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
- List at least two concrete bugs you noticed at the start  
  (for example: "the secret number kept changing" or "the hints were backwards").

  The hints were reversed.
  The new game button does not actually start a new game.
  There is no difference between the different levels - easy, medium and hard.

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).

---

  I used Claude Code Agent.
  One suggestion was moving the entire check_guess function into logic_utils.py and also that it had the incorrect if branch checks (reversed). It changed this, and I verified by running the game through streamlit

  AI gave me a misleading suggesstion about fixing the new game feature, which was moving it to logics_util.py, which would have been inefficient. So, an alternative suggestion it gave me is to change the state variable itself,which was the correct approach.


## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
- Did AI help you design or understand any tests? How?

---

  I checked that a bug was actually fixed by running the game through streamlit.

  Checking if lower and higher was working correctly, I went ahead and manually checked by opening the drop down of "developer debug info". This showed me that my if branch conditions were correct.

  AI developed a new test called pytest, which essentially tested check_guess using a test case approach, as opposed to manual testing.



## 4. What did you learn about Streamlit and state?

- In your own words, explain why the secret number kept changing in the original app.
- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?
- What change did you make that finally gave the game a stable secret number?

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
- In one or two sentences, describe how this project changed the way you think about AI generated code.


