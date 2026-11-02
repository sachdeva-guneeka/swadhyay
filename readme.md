# Swadhyay

**Learn by solving. Learn more by teaching.**

Swadhyay is a gamified quiz platform for students of class 9 to 12 (CBSE, JEE, NEET, CUET). Students earn points and streaks by solving quizzes, and earn double points by creating quizzes that other students learn from.

- Hackathon track: Open-Innovation
- Team: Binary Bizarre
- Live prototype: https://sachdeva-guneeka.github.io/swadhyay/
## The problem

- Most practice apps reward only solving. Creating a quiz earns nothing, so shared content stays thin.
- Student-made answer keys can be wrong, and nothing checks them.
- Points systems break when one person can make many accounts.

## Our idea

Creators are rewarded for how much other students learn from their quizzes, not for how many they upload.

| Action | Points |
| --- | --- |
| Solve a quiz | Up to 10, based on your marks |
| Create a quiz | 20, once the quiz passes the AI check and 5 unique students have played it |
| Daily practice | Streak grows by 1 per day |

Every question needs an explanation, because writing it is part of the learning.

## What the prototype does

- **Practice:** quizzes by class and exam track (CBSE, JEE, NEET, CUET), each track with its own colour.
- **Play:** one question at a time with instant right/wrong feedback and an explanation. Points and streak update at the end.
- **Create a quiz:** a pre-filled form with 4 options, a correct answer and a required explanation per question.
- **AI answer check:** compares each creator answer with a second answer and sends mismatches to review. A demo checkbox forces a disagreement on question 2.
- **My quizzes:** shows "AI check passed" or "Needs review", and a unique-player progress bar out of 5.
- **Leaderboard:** ranks update live as points change.

## What is simulated

This is a front-end prototype. Nothing is saved, and it resets when the page is refreshed.

- The AI check is simulated. No AI service is called.
- Classmates playing your quiz are simulated with a button.
- Phone number OTP login is not built yet.
- Leaderboard names marked "(sample)" are made up.

## How to run

Open `index.html` in a browser. No install or build step is needed. Keep all files from this folder together.

## Planned full version

| Layer | Choice |
| --- | --- |
| Frontend | React and Tailwind CSS |
| Backend | Node.js and Express |
| Database | PostgreSQL |
| Login | Phone number OTP, one account per number |
| AI check | An LLM API that solves each question and flags mismatches with the creator's key |

Anti-abuse rules planned: only unique players count (not the creator), a minimum of 5 questions with explanations, a daily cap on creator rewards, duplicate question detection, a report button, and AI as a flagger with human review making the final decision.

## Roadmap

1. Real phone OTP login and database storage
2. Real AI answer check with human review queue
3. Mistake bank with spaced repetition
4. Creator analytics and learning-outcome bonus points
5. Hindi and regional language support
