# Cursor Tutor Manifesto

This system is made for beginner coders to utilize AI in a safe way so that AI is not used to replace the user's knowledge and skills. It currently consists of 4 modes:

- Tutor Mode
- Act Mode
- Debug Mode
- Plan Mode

The system can also be used with Copilot.

## Modes

### Plan Mode

This is the mandatory starting point for any new project. In this mode, the manifesto acts as a project manager, guiding you through a conversational interview that covers the entire SDLC.

- **Purpose:** To make you think through the software development life cycle _before_ writing a single line of code.
- **Output:** A comprehensive `project_details.md` blueprint file in your project's root. This file serves as the "source of truth" for all other modes.

### Tutor Mode

This is your default day-to-day working mode. The Tutor's primary goal is to help you find the answer, not to give it to you. It will **never write feature code for you.**

- **Purpose:** To guide you through problems using the **Question Driven Development (QDD)** framework.
- **Process:**
  1. It first reads and understands your project_details.md file.
  2. It explains the high-level concepts you're dealing with.
  3. It asks targeted questions to help you break down the problem.
  4. It suggests specific Google queries and documentation pages.
  5. It provides conceptual feedback on your code attempts and quizzes you on your successes.

### Debug Mode

This mode is for when you are stuck on a specific error. It guides you through the process of professional debugging without giving away the solution.

- **Purpose:** To teach you how to systematically find the root cause of an error.
- **Process:**
  1. It forms a hypothesis about the error's cause.
  2. It provides temporary debugging code (like logging statements) and search queries to help you test the hypothesis.
  3. Once the bug is found, it provides a "Post-Mortem Report" explaining the cause, the solution, and how to prevent it in the future.

### Act Mode - Last Resort

This is your "break glass in case of emergency" mode. When you are completely blocked and cannot proceed, ACT mode will step in and write the code for you.

- **Purpose:** To help you overcome a severe blocker so your project can move forward.
- **Process:**
  1. It uses the project_details.md file and a codebase search to determine the best place for the new code.
  2. It provides a detailed Markdown explanation of _why_ the code is designed a certain way.
  3. It generates the code itself, filled with extensive comments explaining _how_ it works.
  4. It quizzes you on the generated code to ensure you understand it.

# How to use

1. Create a new mode in Cursor or Copilot.
2. Apply the following rules to each mode:

- Tutor Mode
  - Tools, only Search
  - Paste rules from `tutor.md` in custom instructions
- Act Mode
  - Tools \- All
  - Turn on Auto Run
  - Paste rules from `act.md` into custom instructions
- Debug Mode
  - Tools \- All
  - Turn on Auto Run
  - Paste rules from `debug.md` into custom instructions
- Plan Mode
  - Run at beginning of project
  - Tools \- Search, and Edit
  - Paste rules from `plan.md` into custom instructions

3. Switch to Plan Mode and type this prompt:
   `let's begin to create the plan for this project`
4. After the plan is created, switch to Tutor Mode and begin to ask questions as you would normally do.
5. Switch to Debug Mode or Act Mode when appropriate.

# Disclaimers

I have not tested this system heavily, so it may not work as expected. Feel free to submit issues or pull requests to help improve it.

# Future Improvements

- [ ] Remove or Modify the QDD framework in Tutor Mode. It is not as helpful as I thought it would be.
- [ ] Add a mode to maintain context between modes. Might be a part of the Tutor Mode or a separate mode.
- [ ] Allow Tutor Mode to write example code to help explain. It cannot be complete code. The goal is to show a brief example of the code and explain it. Could be broken into a separate mode.
- [ ] Allow Tutor Mode to link to documentation more aggressively. I didn't know Cursor could do this so was not using it that heavily.
