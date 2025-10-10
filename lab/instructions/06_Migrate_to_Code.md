# Migrate to Code

In this section, you will learn how to migrate the agent you've created in AI Toolkit to a code-based workflow.

The AI Toolkit provides generated code for agents created in Agent Builder. You can chose your preferred SDK as well as programming language. Once you have your code file, you can integrate your agent into your own app.

## Step 1: Generate the Code

In Agent Builder, scroll down towards the bottom of the left side of the screen and select **View Code**.

![View code button.](../../img/view-code.png)

When prompted, select your preferred client SDK and programming language. Once the new file is created, save the file to your workspace.

## Step 2: View the Code

Before running the script, review the content of the file as there may be placeholders that must be modified before running. If you need assistance understanding the script logic, you could leverage GitHub Copilot Chat in **Ask** mode.

To access GitHub Copilot Chat, select the **Toggle Chat** icon at the top of the Visual Studio Code window.

![Toggle chat button.](../../img/toggle-chat.png)

Just be sure to have the file active so that GitHub Copilot Chat can use the file as context. Alternatively, you could reference the specific file itself in your prompt to GitHub Copilot Chat.

![GitHub Copilot Chat in Ask mode.](../../img/ghcp-ask-mode.png)

If there's any changes that need to be made, you could switch to **Agent** mode and request the changes to be made. You'll be requested to approve any file changes prior to committing the file updates to the script.

## Step 3: Run the Code

If you'd like to run the code, follow the comments at the top of the code file. The instructions will vary as it's dependent on the client SDK and language selected.

## Bonus

Consider using GitHub Copilot Chat in Agent mode to assist with creating files for the Cora agent's UI. You could also ask GitHub Copilot Chat in Agent mode to integrate the agent script into the app UI so that you'll have a working prototype of the agent!

## Key Takeaways

- Agent Builder automatically generates code for agents in multiple programming languages and SDKs, facilitating easy migration from prototype to production.
- Code files may contain placeholders that need modification before execution, requiring developers to understand and adapt the generated logic for their specific needs.
- Using GitHub Copilot Chat in Ask and Agent modes helps developers understand generated code and create additional components like UI elements for complete agent applications.

Click **Next** to proceed to the following section of the lab.