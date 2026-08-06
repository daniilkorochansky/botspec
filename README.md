# Bot Specification Framework
<img width="1400" height="420" alt="botspec_banner" src="https://github.com/user-attachments/assets/676772bb-5ec3-4012-afa7-3a5ab4d20528" />
BotSpec is a platform-independent framework for building chatbots from declarative YAML scenarios. Write your conversation flow once and run it on Telegram, MAX, and other messengers without changing your business logic.

## Features
+ **Platform-Independent Architecture:** You write the dialogue scenario once. The bot launches simultaneously on Telegram, the MAX messenger, and any other platforms without changing the business logic.
+ **Graceful UI Degradation:** Messenger adapters take platform limitations into account. If the MAX messenger does not support native reply buttons, the adapter seamlessly converts them into inline buttons on its own. The logic of the scenario remains intact.
+ **REST-like Router Mapping:** Scenarios are divided into isolated router files with global paths. You can link files together and transition to states in other routers while completely avoiding state ID conflicts.
+ **Mermaid Visualization:** Using the built-in CLI, you can generate finite state machine diagrams in Mermaid format.
+ **Dynamic UI with Jinja2:** The built-in Jinja2 templating engine is embedded directly within YAML files.
+ **State-Machine Managed by Engine:** Developers no longer need to manually manage states. State transitions are fully managed by the declarative core.
+ **Pluggable Session Storage & Isolation:** User sessions are strictly separated by messaging apps. Switching between local storage for testing and distributed Redis for production involves changing a single line in the configuration.
+ **Guard Pattern Actions:** Complete separation of code from the interface using a special Python decorator. Functions work with standard Python data types and can control FSM transitions via return values.
+ **Secure Environment-Driven Config:** The global YAML file that you specify when running the scenario safely retrieves tokens and database credentials from environment variables or the “.env” file using the ${VARIABLE} syntax.
