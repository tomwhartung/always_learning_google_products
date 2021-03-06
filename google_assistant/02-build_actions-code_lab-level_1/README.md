# always_learning_google_assistant/02-build_actions-code_lab-level_1

This subdirectory contains just a README.md file with notes about things learned from the Google Code Labs.

## Glossary and Resources

- For a glossary of terms, see ../GLOSSARY.md
- For links to resources with more information, see ../FOR_MORE_INFORMATION.md

## Directory `02-build_actions-code_lab-level_1`

Requested an increase of 20 projects for my quota.
Apparently the ones I have deleted still count against it, and I have only 2 left.
They will let me know 'typically in about 2 business days.'

- Response to my request is here: https://support.google.com/code/contact/project_quota_increase?authuser=0
- Quota FAQ is here: https://support.google.com/cloud/answer/6330231?authuser=0

**Update on 2018-05-19:** Quota increase approved!

## Steps Taken

### 1.3: Setup

#### 1.3.1. Create an Actions project

- Actions Console -> Add/import project
- "actions-codelab" -> Create Project
- No category -> click on "Skip" up in the corner
- Build -> Actions -> Add your first Action
- Select English -> Click on Update
- Custom intent card -> Click on Build -> Opens a Dialogflow Console in a new tab

#### 1.3.2. Create a Dialogflow agent

- Switch to Dialogflow tab
- Changed default time zone
- Click Create
- Now on Intents page in the Dialogflow window

### 1.4. Starting a conversation

#### 1.4.1. Create a welcome intent

- Click on Default Welcome Intent
- Scroll down to Responses section and delete all (other?) text responses
  - (Trash can icon appears only when hovering over the response)
- Enter new response: "Welcome! What is your favorite color?"
- Click Save (at the top of the page)

### 1.4.2. Test the welcome intent

Using the simulator for this.
For more about the simulator, see https://developers.google.com/actions/tools/simulator

- Menu -> Integrations
- Click on Google Assistant -> Integration Settings (at the bottom)
- A popup appears -> Test (at the bottom)
- Another popup appears, leave Auto-preview changes enabled -> Continue
- Simulator -> "Talk to my test app"
- It responds with "Welcome! What is your favorite color?"
- For more information, see the tabs: Display, Request, etc.

### 1.5. Create conversational responses

#### 1.5.1. Create a Dialogflow intent

- Back to Dialogflow console tab -> Close Google Assistant popup
- Menu -> Intents -> Create
- Name: "favorite color" -> Save
- Click on Add training phrases - add the following expressions:
  - purple is my favorite
  - black is my favorite color
  - i love yellow
  - Pink
  - my favorite color is green
- Action and parameters -> Manage Parameters And Action
- Check the Required box next to color
- Click on Define prompts...
- Enter "What's your favorite color?" and click Close
- Scroll down to the Fulfillment section in this page -> Enable Fulfillment
- Turn on the "Enable webhook call for this intent" switch -> Save (at the top)

### 1.6. Implement a webhook

#### 1.6.1. Build your webhook

- Dialogflow Menu -> Fulfillment -> Inline Editor -> Enable
- Copy and paste code into index.js
- Click Deploy button
- Note use of color variable in the code
- This corresponds to the color variable set up in the Intents menu option

#### 1.6.2. Test the action

- Return to Actions Console window and select the project
- Click on Simulator and enter "Talk to my test app"

Links to more information:

- More about fulfillment: https://dialogflow.com/docs/how-tos/getting-started-fulfillment
- More about the simulator: https://developers.google.com/actions/tools/simulator
- More about actions: https://developers.google.com/actions/
- Github repos for actions on google: https://github.com/actions-on-google/
- Dialogflow home page - primary source for docs: https://dialogflow.com/

## Local Copy of the Code

Cloned the repo for the google assistant code labs at:

- https://github.com/actions-on-google/codelabs-nodejs

into directory

- `/var/www/always_learning/google_assistant_codelabs/codelabs-nodejs`


