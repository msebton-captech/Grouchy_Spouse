# GrouchySpouse

A fun project that leverages multi-platform audio to produce a grouchy version of your spouse or partner. Change the system prompt by modifying system_prompt.txt. Easy!  

![th](https://github.com/user-attachments/assets/36968083-6b90-4130-9c1d-fd47780737de)


## Features

- Chat with an AI-powered assistant
- Maintains conversation history for context-aware responses
- Synthesizes and plays audio responses

## Prerequisites

- .NET SDK
- An API token for OpenAI
- A key for Azure AI Speech Service


## Setup

1. Clone the repository:
    ```sh
    git clone https://github.com/msebton-captech/Grouchy_Spouse.git
    ```

2. Review the ```system_prompt.txt``` file in the project directory. If necessary, modify it to your desired system prompt content.

3. Update the API keys in the ```InitializeClients``` method in ``Program.cs``:
    ```csharp
    openAiToken = config["OpenAiToken"];
    subscriptionKey = config["SpeechServiceSubscriptionKey"];
    subscriptionRegion = config["SpeechServiceRegion"];
    ```  
    You can create a json configuration file to hold your keys such as in this example:  
    ```json
    {
        "OpenAiToken": "YOUR_OPEN_AI_TOKEN",
        "SpeechServiceSubscriptionKey": "YOUR_AZURE_AI_SPEECH_SERVICE_KEY",
        "SpeechServiceRegion": "eastus" // your azure region
    }
    ```

4. Build and run the project:
    ```sh
    dotnet build
    dotnet run
    ```

## Usage

1. Run the application:
    ```sh
    dotnet run
    ```

2. Start chatting with the AI assistant by typing your messages in the console.

3. The AI assistant will respond with text and synthesized audio.

## License

This project is licensed under the MIT License. See the LICENSE file for details.
