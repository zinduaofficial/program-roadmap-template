# Project: Number Guessing Game

> **Course:** Python Fundamentals  
> **Type:** Individual  
> **Duration:** Week 2 assignment  
> **Level:** Beginner

## Project Overview

Build an interactive command-line number guessing game where the computer generates a random number and the player tries to guess it. The game should provide feedback on each guess, track attempts, implement difficulty levels, and save high scores to a file. This project reinforces your understanding of control flow, functions, and file handling.

## Learning Objectives

By completing this project, students will:
- Apply conditional statements and loops in a real application
- Create and use functions to organize code
- Handle user input and validate data
- Work with random number generation
- Implement file I/O for data persistence
- Design a user-friendly command-line interface

## Project Description

Create a fun and engaging number guessing game that challenges players to guess a randomly generated number within a certain number of attempts. The game should adapt to different difficulty levels and keep track of the best performances.

### User Story / Problem Statement

**As a** game player,  
**I want** to play a number guessing game with different difficulty levels,  
**So that** I can challenge myself and compete for the best score.

## Requirements

### Functional Requirements

The project must:
1. Generate a random number within a range that varies by difficulty level
2. Accept player guesses and provide feedback (too high, too low, correct)
3. Track the number of attempts used
4. Implement three difficulty levels (Easy, Medium, Hard)
5. Calculate and display a score based on attempts and difficulty
6. Save high scores to a file
7. Display the top 5 high scores
8. Allow the player to play multiple rounds
9. Validate all user inputs and handle errors gracefully
10. Provide clear instructions and feedback throughout the game

### Technical Requirements

**Technology Stack:**
- Python 3.10+ - Core programming language
- random module - For number generation
- json module - For storing high scores

**Architecture:**
- Modular design with functions for different game operations
- Separate concerns (game logic, I/O, data persistence)

**Code Quality:**
- Follow PEP 8 style guidelines
- Include docstrings for all functions
- Use meaningful variable and function names
- Handle edge cases and invalid inputs

## Features

### Core Features (Required)
- [ ] **Random Number Generation:** Generate numbers within appropriate ranges based on difficulty
- [ ] **Difficulty Levels:** Easy (1-50), Medium (1-100), Hard (1-200)
- [ ] **Guess Feedback:** Inform player if guess is too high, too low, or correct
- [ ] **Attempt Tracking:** Count and display number of attempts
- [ ] **Score Calculation:** Calculate score based on attempts and difficulty (fewer attempts = higher score)
- [ ] **High Score Persistence:** Save top scores to a JSON file
- [ ] **High Score Display:** Show top 5 high scores with player names
- [ ] **Input Validation:** Ensure guesses are valid numbers within range
- [ ] **Replay Option:** Allow playing multiple rounds without restarting program

### Advanced Features (Optional/Bonus)
- [ ] **Hints System:** Offer limited hints (e.g., "is the number even/odd?")
- [ ] **Timer:** Track and display time taken to guess
- [ ] **Leaderboard:** Separate leaderboards for each difficulty level
- [ ] **ASCII Art:** Add visual flair to the game interface
- [ ] **Custom Range:** Allow players to set custom number ranges

## Specifications

### Game Flow
```
1. Display welcome message and instructions
2. Ask player for name
3. Ask player to select difficulty level
4. Generate random number based on difficulty
5. Enter game loop:
   - Prompt for guess
   - Validate input
   - Provide feedback
   - Increment attempt counter
   - Check if correct
6. Calculate score
7. Update high scores if applicable
8. Display high scores
9. Ask if player wants to play again
10. If yes, go to step 3; if no, exit
```

### Difficulty Specifications
- **Easy:** Range 1-50, max 10 attempts for perfect score
- **Medium:** Range 1-100, max 12 attempts for perfect score
- **Hard:** Range 1-200, max 15 attempts for perfect score

### Score Calculation
```
Base Score = (Max Attempts for Perfect Score - Actual Attempts + 1) * Difficulty Multiplier
Difficulty Multiplier: Easy = 10, Medium = 20, Hard = 30
Score cannot be negative
```

### High Score Data Structure
```json
{
  "scores": [
    {
      "name": "Player Name",
      "score": 100,
      "attempts": 5,
      "difficulty": "Medium",
      "date": "2025-12-07"
    }
  ]
}
```

## Getting Started

### Prerequisites
Before starting this project, ensure you have:
- Completed Week 1 and Week 2 of Python Fundamentals
- Python 3.10+ installed
- Basic understanding of functions, loops, and conditionals

### Setup Instructions
1. Create a new file called `number_guessing_game.py`
2. Create a `highscores.json` file (or let the program create it)
3. Import required modules: `random`, `json`, `datetime`
4. Plan your functions before coding

## Deliverables

Students must submit:

1. **Source Code**
   - `number_guessing_game.py` - Main game file
   - Well-organized code with clear function separation
   - Comments explaining complex logic
   
2. **Documentation**
   - README.md explaining how to run the game
   - Description of how your score calculation works
   - Any design decisions or bonus features implemented
   
3. **Demonstration**
   - Screenshot or recording showing:
     - A complete game round
     - High score display
     - Input validation handling an invalid input

## Assessment Criteria

Projects will be evaluated on:

| Criterion | Weight | Description |
|-----------|--------|-------------|
| Functionality | 40% | All core features work correctly |
| Code Quality | 25% | Clean, well-organized, follows PEP 8 |
| User Experience | 15% | Clear instructions, good feedback, easy to use |
| Error Handling | 10% | Handles invalid inputs gracefully |
| Documentation | 10% | Clear README and code comments |

### Rubric

**Excellent (90-100%):**
- All features work perfectly
- Exceptional code organization and documentation
- Implements at least one bonus feature
- Excellent user experience with clear feedback

**Good (80-89%):**
- All core features work correctly
- Good code organization and style
- Adequate documentation
- Handles most error cases

**Satisfactory (70-79%):**
- Most features work with minor issues
- Acceptable code organization
- Basic documentation
- Some error handling

**Needs Improvement (<70%):**
- Missing core features or significant bugs
- Poor code organization
- Minimal documentation
- Inadequate error handling

## Timeline & Milestones

**Suggested Timeline:**

| Day | Milestone | Description |
|-----|-----------|-------------|
| 1 | Planning | Design functions, plan game flow |
| 2 | Core Game | Implement basic guessing logic |
| 3 | Features | Add difficulty levels, validation |
| 4 | Persistence | Implement high score saving |
| 5 | Polish | Test thoroughly, improve UX |

**Key Deadlines:**
- Planning Complete: Day 1
- Core Game Working: Day 2
- Final Submission: End of Week 2

## Resources

### Documentation
- Python random module: https://docs.python.org/3/library/random.html
- Python json module: https://docs.python.org/3/library/json.html
- Input validation techniques

### Tutorials
- Working with JSON in Python
- Python random number generation
- Creating command-line menus

## Helpful Tips

1. **Start Simple**
   - Get the basic game working first (fixed range, no difficulty)
   - Add features incrementally
   - Test each feature before moving to the next

2. **Function Organization**
   - Create separate functions for: getting input, validating input, playing one round, managing high scores, displaying menu
   - Keep functions focused on one task

3. **Testing**
   - Test edge cases (guessing 0, negative numbers, letters)
   - Test all difficulty levels
   - Verify high scores save and load correctly

## Common Challenges

**Challenge 1:** High scores not persisting between runs  
**Solution:** Ensure you're writing to and reading from the JSON file correctly. Check file paths and permissions.

**Challenge 2:** Input validation getting messy  
**Solution:** Create a dedicated function for input validation that returns a valid number or None.

**Challenge 3:** Score calculation seems off  
**Solution:** Test your formula with example values. Make sure you're handling the case where attempts exceed the perfect score threshold.

## Extension Ideas

For students who finish early or want to go further:
- Add a "give up" option that reveals the answer
- Implement sound effects or visual animations
- Create a two-player mode
- Add achievements (e.g., "Perfect Score", "Lucky Guess")
- Build a graphical interface using tkinter

## Submission

**How to Submit:**
1. Ensure your code runs without errors
2. Complete the README.md with game instructions
3. Test all features thoroughly
4. Push to your GitHub repository
5. Submit the repository link

**Submission Checklist:**
- [ ] All core features implemented and working
- [ ] Code follows PEP 8 style guidelines
- [ ] README.md completed with instructions
- [ ] High scores persist between game sessions
- [ ] Input validation handles all edge cases
- [ ] Code includes function docstrings
- [ ] Tested on fresh Python installation

---

**Questions?** Ask in class, office hours, or on Slack  
**Last Updated:** December 2025
