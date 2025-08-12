# Manage Learning Memory Bank

## ⚠️ CRITICAL EXECUTION NOTICE ⚠️

**THIS IS AN EXECUTABLE WORKFLOW - NOT REFERENCE MATERIAL**

When this task is invoked, you must follow these steps precisely.

## Processing Flow

1.  **Prompt for Learning:**
    *   Ask the user: "Please state the new learning you would like to add to the memory bank."
    *   Wait for the user's response and store it as the "learning".

2.  **Identify Agent:**
    *   Ask the user: "Which agent should be credited with this learning?"
    *   Wait for the user's response and store it as the "agent".

3.  **Read Memory Bank:**
    *   Read the contents of `{root}/data/learning-memory-bank.json`.
    *   Parse the JSON content into an array.

4.  **Append New Learning:**
    *   Create a new JSON object with the following structure:
        ```json
        {
          "learning": "<the learning provided by the user>",
          "agent": "<the agent name provided by the user>",
          "timestamp": "<current ISO 8601 timestamp>"
        }
        ```
    *   Add this new object to the array.

5.  **Write Memory Bank:**
    *   Convert the updated array back into a formatted JSON string.
    *   Overwrite the `{root}/data/learning-memory-bank.json` file with the new JSON string.
    *   Inform the user that the learning has been successfully added.
