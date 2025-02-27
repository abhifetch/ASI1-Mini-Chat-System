# ASI1-Mini-Chat-System

## Overview
The ASI1 Chat System is a modular, agent-based chat system leveraging the uAgents framework. It
facilitates seamless communication between a Client Agent and a Server Agent to process and respond
to user queries in real time. The system integrates an external API (ASI1 API) to generate intelligent
responses, making it a powerful tool for AI-driven applications.

## System Architecture
### Components:
1.  Server Agent (asi1_chat_agent)
  - Listens for incoming queries.
  - Calls the ASI1 API to process the query.
  - Sends the API's response back to the client agent.

2.  Client Agent (asi1_client_agent)
  - Interacts with the user to collect input.
  - Sends the query to the server agent.
  - Receives and displays the response to the user.


## Workflow
1.  Client Agent Initialization
  - The client agent starts and prompts the user for a query.
    
2.  Sending the Query
  - The client agent constructs an ASI1Query message containing:
  - The user's query.
  - The client agent's address.
  - This message is sent to the server agent.
    
3.  Server Agent Processing
  - The server agent receives the ASI1Query.
  - It calls the ASI1 API to generate a response.

4.  Returning the Response
  - The server agent receives the API response.
  - Sends the response back to the client agent via an ASI1Response message.

5.  Displaying the Response
  -The client agent receives the response and displays it to the user.

## Example Interaction

```
User: Ask something: Give me the top 5 downloaded Hugging Face models for 
image classification

Client Agent -> Server Agent: Sends query

Server Agent -> ASI1 API: Calls API
ASI1 API Response:
1. facebook/deit-base-distilled-patch16-224
2. google/vit-base-patch16-224
3. microsoft/resnet-50
4. nvidia/mit-b0
5. efficientnet-b0

Server Agent -> Client Agent: Sends response
Client Agent: Displays the response to the user
```

## Benefits
  - **Scalability** – Can scale with additional agents or extended functionalities.
  - **Modularity** – Separation of concerns between client and server agents.
  - **Real-time Interaction** – Enables dynamic user-agent communication.
  - **API Integration** – Showcases how external APIs can enhance AI-driven applications.

## Use Cases
  - AI-powered chatbots
  - Customer support automation
  - Interactive knowledge assistants

## Conclusion
The **ASI1 Chat System** demonstrates a robust **agent-based** approach to building intelligent, interactive
applications. With its modular architecture and seamless API integration, this system is a great
foundation for exploring **autonomous agent interactions** in AI-powered environments.
