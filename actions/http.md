# HTTP Actions

[Back to Top](#http-actions) | [Next: Function Code Actions (function-code.md)](#function-code-actions-function-codemd)

This document explains how to create HTTP Actions in MintMini. HTTP Actions allow you to integrate with external APIs and services by sending HTTP requests.

## What are HTTP Actions?

HTTP Actions enable your AI Agent to interact with the real world by sending HTTP requests to external APIs and services. This allows you to retrieve data, trigger actions, and automate tasks using web services.

## Creating HTTP Actions

To create a new HTTP Action in MintMini:

1.  Go to the Actions configuration panel.
2.  Click "+ Create" to start creating a new Action.
3.  Enter the relevant information for the Action:
    *   **Action Name:** A name to be shown to the user.
    *   **Icon Url:** A URL to an icon for the Action.
    *   **Overview:** Describe to the users what your plugin does and how to use it with examples. Markdown is supported.
4.  Choose `HTTP` type
5.  Configure the HTTP request:
    *   **HTTP Method:** Select the HTTP method (GET, POST, PUT, DELETE, etc.).
    *   **Endpoint:** Enter the URL of the API endpoint.
    *   **Headers:** Add any required HTTP headers (in JSON format).
        *   Example:
            ```json
            {
              "Content-Type": "application/json",
              "Authorization": "Bearer YOUR_API_KEY"
            }
            ```
    *   **Body:** Enter the request body (in JSON format).
        *   Example:
            ```json
        	{
			  "query": {
			    "type": "function_spec",
			    "mapKey": "query"
			  },
			  "search_depth": {
			    "type": "function_spec",
			    "mapKey": "search_depth"
			  },
			  "include_answers": {
			    "type": "function_spec",
			    "mapKey": "include_answers"
			  }
			}
            ```
    *   **Query:** Enter the request query (in JSON format).
    *   You can use these variables in Request URL, Request Body, Request Query and Request Headers.

## Tips for Effective HTTP Actions

*   **Understand the API:** Familiarize yourself with the API you are integrating with, including its endpoints, request parameters, and authentication requirements.
*   **Handle Responses:** Implement error handling to gracefully handle API errors and unexpected responses.
*   **Secure Your API Keys:** Store API keys and other sensitive information securely.

With HTTP Actions, you can create a powerful and versatile AI Agent that can automate a wide range of tasks. 🎉
