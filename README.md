
# gmailGPT Autoresponder

This is a Python script that uses the Gmail API and OpenAI's GPT-3.5-turbo model to automatically respond to unread emails in Gmail. The script reads the user's Gmail inbox, selects an unread email, generates a response using the GPT-3.5-turbo model, and sends the response back to the sender.

## Prerequisites

Before running the script, you need to set up a few things:

### Install the required Python packages:

```
pip install google-auth google-auth-oauthlib google-auth-httplib2 google-api-python-client openai
```

### Enable the Gmail API:
- Go to the Google Cloud Console.
- Create a new project or select an existing one.
- Enable the Gmail API for your project.
- Create credentials (OAuth client ID) for the project.
- Download the credentials file (JSON format) and save it as credentials.json in the same directory as the script.

### Obtain an OpenAI API key:
- Sign up for an account on the OpenAI website.
- Create an API key and save it to a file named openai-api-key.txt in the same directory as the script.
- Create the necessary directories and files:
- Create a directory named modes.
- Inside the modes directory, create subdirectories for each classification role you want to use (e.g., modes/role1, modes/role2).
- Inside each role directory, create a file named role.txt that contains the name of the role.


### Usage

Run the script using the following command:

```
python gpt3.py [email]
```

Replace [email] with the email address associated with the Gmail account you want to use.

The script will continuously check the Gmail inbox for unread emails and respond to them using the GPT-3.5-turbo model. It selects the classification role and generates a response based on the email's sender, subject, and snippet. The response is then sent back to the sender.

Please note that the script responds to one email at a time and waits for two seconds before checking the inbox again.

### License

This project is licensed under the MIT License.
