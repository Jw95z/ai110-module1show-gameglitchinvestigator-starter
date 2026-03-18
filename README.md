# 🎮 Game Glitch Investigator: The Impossible Guesser

## 🚨 The Situation

You asked an AI to build a simple "Number Guessing Game" using Streamlit.
It wrote the code, ran away, and now the game is unplayable. 

- You can't win.
- The hints lie to you.
- The secret number seems to have commitment issues.

## 🛠️ Setup

1. Install dependencies: `pip install -r requirements.txt`
2. Run the broken app: `python -m streamlit run app.py`

## 🕵️‍♂️ Your Mission

1. **Play the game.** Open the "Developer Debug Info" tab in the app to see the secret number. Try to win.
2. **Find the State Bug.** Why does the secret number change every time you click "Submit"? Ask ChatGPT: *"How do I keep a variable from resetting in Streamlit when I click a button?"*
3. **Fix the Logic.** The hints ("Higher/Lower") are wrong. Fix them.
4. **Refactor & Test.** - Move the logic into `logic_utils.py`.
   - Run `pytest` in your terminal.
   - Keep fixing until all tests pass!

## 📝 Document Your Experience

- [ ] Describe the game's purpose. The purpose of the game is to let the player guess a random number based on the selected difficulty while giving hints, tracking attempts, and updating the score.
- [ ] Detail which bugs you found. I found that the high and low hints were backwards, the attempts counter did not update correctly on the first guess, and the hint checkbox did not show the previous hint again unless I pressed submit.
- [ ] Explain what fixes you applied. I fixed the hint logic in check_guess, changed the attempts value so it starts at 0 instead of 1, and improved the hint behavior by storing and showing the last hint correctly. I also moved the main game logic into logic_utils.py to make the code easier to test and maintain.

## 📸 Demo

- [ ] ![Insert a screenshot of your fixed, winning game here](https://github.com/user-attachments/assets/e291e494-add2-4f49-922f-4f0d63c545b4)

## 🚀 Stretch Features

