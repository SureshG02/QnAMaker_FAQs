# QnA Maker

Bot Framework v4 QnA Maker bot sample

This bot has been created using [Bot Framework](https://dev.botframework.com), it shows how to create a bot that uses the [QnA Maker Cognitive AI](https://www.qnamaker.ai) service.

The [QnA Maker Service](https://www.qnamaker.ai) enables you to build, train and publish a simple question and answer bot based on FAQ URLs, structured documents or editorial content in minutes. In this sample, we demonstrate how to use the QnA Maker service to answer questions based on a FAQ text file used as input.

## Prerequisites

This samples **requires** prerequisites in order to run.

### Overview

This bot uses [QnA Maker Service](https://www.qnamaker.ai), an AI based cognitive service, to implement simple Question and Answer conversational patterns.

We will be creating knowledge base for digia 112 FAQs using URL https://digia.com/en/112-suomi/frequently-asked-questions/. 

Please refer manual about how to make QnA KB using URL.


- [Node.js](https://nodejs.org) version 10.14 or higher

    ```bash
    # determine node version
    node --version
    ```

## To try this sample

- Clone the repository OR download as zip from dropdown.

    ```bash
    git clone https://github.com/SureshG02/QnAMaker_FAQs.git
    ```

- In a terminal, navigate to `/QnAMaker_FAQs` folder


- Install modules

    ```bash
    npm install
    ```

- Setup QnAMaker

    Please refer manual to set up QnA for 112 digia FAQs.


- Run the sample

    ```bash
    npm start
    ```

## Testing the bot using Bot Framework Emulator

[Bot Framework Emulator](https://github.com/microsoft/botframework-emulator) is a desktop application that allows bot developers to test and debug their bots on localhost or running remotely through a tunnel.

- Install the Bot Framework Emulator version 4.3.0 or greater from [here](https://github.com/Microsoft/BotFramework-Emulator/releases)

### Connect to the bot using Bot Framework Emulator

- Launch Bot Framework Emulator
- File -> Open Bot
- Enter a Bot URL of `http://localhost:3978/api/messages`

## Deploy the bot to Azure

## Prerequisites

Install Azure CLI

https://docs.microsoft.com/en-us/cli/azure/install-azure-cli?view=azure-cli-latest

Use below commands to deploy to cloud.

az login

az account set --subscription "subscription-id"

## Go to QnAMaker_FAQs directory and run below command

az bot prepare-deploy --code-dir "." --lang Javascript

## Zip QnAMaker_FAQs folder and run below command from directory where zip file exists.

az webapp deployment source config-zip --resource-group "<resource-group-name>" --name "<name-of-web-app>" --src "code.zip"
