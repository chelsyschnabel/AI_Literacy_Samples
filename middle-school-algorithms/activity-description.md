# AI Literacy: 7th and 8th Grades

## Overview

For this activity, students will write an step-by-step algorithm for a number guessing game. They will utilize AI to help them improve upon their algorithm and optimize the algorithm before any code is written. The intention is to have the students utilize AI to assist them in improvements and brainstorming as opposed to completing the assignment for them.

**Subject:** Computer Science - Algorithm Design  

**Suggested Tool:** Claude for pseudocode review or district/school-provided AI tool

**Learning Objective:** Using AI to improve algorithm efficiency and clarity

## Student Work Sample: "Number Guessing Game Algorithm"

**Initial Algorithm (Student's First Draft):**
```
START
1. Computer picks random number 1-100
2. Ask user to guess
3. If guess is right, say "correct" and stop
4. If guess is wrong, say "try again"
5. Go back to step 2
END
```

**AI Consultation for Improvement:**
*Student's prompt:* "I wrote this algorithm for a guessing game. Can you help me identify what could be improved? I want to make it more helpful for players but don't want you to rewrite it for me."

*AI feedback summary:*
- Algorithm works but could be more user-friendly
- Consider giving players hints (higher/lower)
- Think about limiting guesses to make it more challenging
- Consider how to handle invalid inputs

**Student's Refined Algorithm:**
```
START
1. Computer picks random number 1-100
2. Set guess_count = 0
3. Ask user to guess (must be 1-100)
4. Add 1 to guess_count
5. If guess equals secret number:
   - Say "Correct! You won in [guess_count] tries!"
   - STOP
6. If guess_count equals 7:
   - Say "Game over! The number was [secret number]"
   - STOP
7. If guess is too high, say "Too high, try lower"
8. If guess is too low, say "Too low, try higher"
9. Go back to step 3
END
```

**Student's Learning Reflection:**
"Using AI to review my algorithm helped me think like a user, not just a programmer. I didn't ask AI to fix my code, but to point out what could be better. This made me realize I needed to give players more information and set limits to make the game fair and fun."
