# Setup Tools: Connect a MCP Server to the Agent

In this section, you will learn how to give your agent access to tools via a Model Context Protocol (MCP) sever. MCP is a powerful, standardized framework that optimizes communication between Large Language Models (LLMs) and external tools, applications, and data sources.

We'll give the Cora agent access to Zava's locally run **Basic Customer Sales** MCP server. This server consists of a **get_products_by_name** tool which enables Cora to do product searches by name with fuzzy matching, get store-specific product availability through row level security, and get real-time inventory levels and stock information.

## Step 1: Start the MCP server

Earlier in the **Model Augmentation** exercise, we added grounding data to the model in the form of a `zava_product_catalog.json` file attachment. While that may have been convenient for the sake of testing the base model prior to model selection, what we'd recommend is to ground the agent with data in such a way that's scalable and adaptable to Zava's changing inventory. Zava's **Basic Customer Sales** MCP server works best for this scenario. For this lab, we'll run the server locally.

To start the **Basic Customer Sales** server, within your Visual Studio Code workspace, navigate to `.vscode/mcp.json`. Within the `mcp.json` file, locate the `zava-customer-sales-stdio` server and click **Start** above the server.

[image]

## Step 2: Add a Tool to the Agent

The **Basic Customer Sales** server consists of two tools:
- get_products_by_name
- 

For this lab, we'll only use the **get_products_by_name** tool. Ideally, you'll only want to give your agent access to tools that are relevant for it's purpose.

Back in Agent Builder, select the **+** icon next to **Tools** to open the wizard for adding tools to the agent. When prompted, select the running **Basic Customer Sales** server followed by the **get_products_by_name** tool.

[image]

## Step 3: Chat with the Agent

You're now ready to test whether the Cora agent executes a tool call when given a prompt that warrants leveraging a tool! On the **Playground** tab, attach the `name-of-image.jpg` and submit the following prompt:

```
Here’s a photo of my living room. Based on the lighting and layout, recommend either a Zava eggshell or Zava semi-gloss paint.
```

If the agent wants to call a tool, a notification will appear in Visual Studio Code requesting [what it'll request]. Select [whatever it says] to execute the tool call.

[image]

Assuming the agent executes a tool call, a section appears for [whatever it's called]. This section indicates which tool was used to aid in generating the agent's output.

[image]

Did Cora recommend Zava's eggshell paint? Hopefully so! Due to the non-deterministic nature of language models, the agent's output will differ each time the aforementioned prompt is submitted. Provided below is example of the agent's response:

[insert agent response]

If the Cora agent did not recommend an eggshell paint, there's various techniques that we could leverage to modify the agent's behavior to encourage the use of the **get_products_by_name** tool. One should way would be to modify the **Instructions** to explicitly reference the required tools to use in which the model has access. Alternatively, you could modify the prompt itself to the following:

```
Recommend a Zava eggshell paint.
```

If you'd like to continue testing tool calls with the Cora agent, try submitting the following prompts in the Playground:

- How much is Zava's eggshell paint?
- What are the current inventory levels for Zava's eggshell paint?
- TBD

## Key Takeaways

- TBD
- TBD
- TBD

Click **Next** to proceed to the following section of the lab.