# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
  - It look like the game of guessing random numbers between 1 to 100, but I think the hints is backward though. 
- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").
  1. As it says, the hint was backward.
  2.  Also I think if I uncheck the show hints, it actually hide the hints, but when I reclick it, the hints does not come out. It comes back when I press the submit button
  3. When I first click the submit, it should decrease the number of attempts, but it did not. I have to click the submit button one more time to see the attempts actually decrease by 1. 

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)? 
  - Copilot
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
  - In check_guess, if guess and secret are not the same type (e.g., one is an int, the other is a string), the comparison may not work as intended.
- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).
  - For example, if guess is an integer and secret is a string (or vice versa), the comparison logic may not behave as expected, resulting in hints like "Go HIGHER!" or "Go LOWER!" that do not match the actual guess.

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed? 
  - I checked the bug in the actual Streamlit game and made sure the behavior matched what I expected. I also made sure the fix did not break other parts of the app.
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
  - One test I ran was entering a guess higher than the secret number. After fixing the code, the game correctly showed the hint to go lower. I also tested the attempts counter and saw that it updated correctly after the first guess once I changed the starting value.
- Did AI help you design or understand any tests? How?
  - Yes, AI helped me think of simple test cases, like checking guesses above and below the secret number. It helped me understand what behavior I needed to verify.

---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?
  - I would explain it by saying that Streamlit basically reruns the whole script every time the user interacts with the app, like when they click a button, type something, or change a checkbox. Because the script keeps rerunning from top to bottom, session_state is what lets the app remember important values like the secret number, score, attempts, and previous hints. Without session state, the app would forget everything every time the page updated.
---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
  - I want to keep fixing one bug at a time and testing after each change.
- What is one thing you would do differently next time you work with AI on a coding task?
  - Next time, I would check AI suggestions more carefully before accepting them.
- In one or two sentences, describe how this project changed the way you think about AI generated code.
  - This project taught me that AI-generated code can look correct but still have logic bugs. I learned that I need to review and test it instead of trusting it right away.
