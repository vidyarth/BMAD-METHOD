# Clarify Task Requirements

## ⚠️ CRITICAL EXECUTION NOTICE ⚠️

**THIS IS AN EXECUTABLE WORKFLOW - NOT REFERENCE MATERIAL**

When this task is invoked:

1. **DISABLE ALL EFFICIENCY OPTIMIZATIONS** - This workflow requires full user interaction.
2. **MANDATORY STEP-BY-STEP EXECUTION** - Each section must be processed sequentially.
3. **NO SHORTCUTS ALLOWED** - You must complete this clarification workflow before proceeding with the main task.

## Processing Flow

1.  **Review Past Learnings:**
    *   Read the contents of `{root}/data/learning-memory-bank.json`.
    *   If the file contains any entries, display them to the user in a numbered list.
    *   Ask the user if any of these past learnings apply to the current task.

2.  **Initial Clarification:**
    *   State the user's initial request.
    *   Ask the user: "Based on your request, I have some initial questions to ensure I understand your goal completely. Shall we begin?"

3.  **Interactive Clarification Loop:**
    *   If the user agrees, begin an interactive loop.
    *   In each iteration of the loop, ask one or more clarifying questions. You should formulate these questions based on your current understanding of the task and what information you believe is missing.
    *   After asking the questions, present the user with the following numbered options:
        1.  "Yes, the requirements are now clear. Please proceed with the task."
        2.  "I have more clarifications to provide."
        3.  "I would like to add a new learning to the memory bank."
    *   Wait for the user's response.

4.  **Loop Actions:**
    *   If the user chooses option 1, exit this clarification task and proceed with the main task.
    *   If the user chooses option 2, continue the loop. Ask the user for their additional clarifications and then formulate new questions if needed.
    *   If the user chooses option 3, execute the `manage-memory-bank.md` task. After the task is complete, return to the clarification loop.

5.  **General Principle:**
    *   Your goal is to achieve 100% certainty about the user's requirements. Do not exit this clarification task until you are confident that you understand the task completely and the user has confirmed it.
