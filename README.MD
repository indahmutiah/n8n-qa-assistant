# n8n-qa-assistant

## INTRO
This is a n8n node that can be used to create a QA Assistant. It can be used to classify user message and then send the message to the right node.

There are 3 roles:
- Product Analyst
- Technical Analyst
- QA Engineer

## TRIGGER
- Telegram

## CREDENTIALS
- Telegram

## RESOURCES
- OpenAI
- OpenRouter
- Google Sheets

## NODES
### Telegram Trigger
This node will trigger the workflow when a message is received on the Telegram channel.

### OpenRouter Chat Model
This node will use OpenRouter to generate a response based on the input message.

### Simple Memory
This node will store the input message in memory.

## Agent Classifier
This node will classify the user message and then send the message to the right node. Specify the role of the user as QA Engineer.

### Switch
This node will switch between the different nodes based on the role of the user. The role of the user is specified by the classifier node.

### AGENT PRD
This node will send a message to the Telegram channel. Specisify the role of the user as Product Analyst.

### AGENT TRD
This node will send a message to the Telegram channel. Specisify the role of the user as Technical Analyst.

### Agent Test Case
This node will send a message to the Telegram channel. Specisify the role of the user as QA Engineer and ganarate the test cases.