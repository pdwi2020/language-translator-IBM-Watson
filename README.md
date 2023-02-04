# language-translator-IBM-Watson

# Getting started with Language Translator

IBM Watson™ Language Translator allows you to translate text programmatically from one language into another language. This tutorial walks you through the commands to translate text from English to Spanish, and to identify the language of a text sample.

The tutorial uses the curl command-line utility to demonstrate REST API calls. For more information about curl, see Using curl with Watson examples.

## Before you begin

Create an instance of the service:
Go to the Language Translator page in the IBM Cloud catalog.
Sign up for a free IBM Cloud account or log in.
Read and agree to the terms of the license agreement.
Click Create.
Copy the credentials to authenticate to your service instance:
View the Manage page for the service instance:

If you are on the Getting started page for your service instance, click the Manage entry in the list of topics.
If you are on the Resource list page, expand the AI / Machine Learning grouping in the Name column, and click the name of your service instance.
On the Manage page, click Show Credentials in the Credentials box.
Copy the API Key and URL values for the service instance.
This tutorial uses an API key to authenticate. In production, use an IAM token. For more information see Authenticating to IBM Cloud.

## Step 1: Translate text

Use the following example to translate two phrases, "Hello, world" and "How are you?" from English to Spanish.

In the command, model_id identifies the model to be used for translation, in this case en-es.
Replace {apikey} and {url} with your service credentials.

curl -X POST --user "apikey:{apikey}" --header "Content-Type: application/json" --data '{"text": ["Hello, world.", "How are you?"], "model_id":"en-es"}' "{url}/v3/translate?version=2018-05-01"
The /v3/translate method accepts a maximum of 50 KB of input text encoded in UTF-8 format for translation.

## Step 2: Identify language

Use the following example to identify the language of text.

Replace {apikey} and {url} with your service credentials.

curl -X POST --user "apikey:{apikey}" --header "Content-Type: text/plain" --data "Language Translator translates text from one language to another" "{url}/v3/identify?version=2018-05-01"

## Step 3: Translate a document

Language Translator allows you to translate documents, such as markup files that use XML or HTML, or Microsoft Office and Open Office files, while retaining the original formatting. For a tutorial, check out Translating documents.

## Next steps

Learn how to customize Language Translator to work for your use case
View the API & SDK reference
Explore sample applications
View language support information:
Supported languages for translation
Identifiable languages
