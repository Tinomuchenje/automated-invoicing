# Intelligent Invoicing Workflow

This README provides an overview and setup instructions for the "Intelligent Invoicing" n8n workflow.

## Overview

The "Intelligent Invoicing" workflow is designed to automate the processing of invoices. It integrates various services such as webhooks, database operations, and AI language models to handle invoice data, extract information, and interact with a Postgres database to store and retrieve invoice details and line items.

![Intelligent Invoicing Workflow Diagram](/images/workflowpicture.png)


Watch the demo [![Watch the demo video](/images/demo-thumbnail.png)](https://drive.google.com/file/d/1f7nTpdGAobaGhbfCs45dRpFxlWvLYoxD/view?usp=sharing)

## Functionality

- **Webhook Endpoint**: Accepts incoming POST requests with authentication and processes queries with user and session information.
- **Input Processing**: Extracts key fields from incoming requests such as query, user_id, request_id, and session_id.
- **Database Integration**: Uses a Postgres database to store messages and maintain conversation history.
- **AI Language Model**: Utilizes OpenAI's language model to process and analyze text.
- **Invoice Processing**: Extracts and structures information from invoice images into a consistent JSON format for database records.
- **Google Drive Integration**: Monitors a specific folder for new invoice images to process.
- **Data Validation and Transformation**: Ensures the accuracy and consistency of the invoice data before it enters the database.

## Setup

1. **n8n Installation**: Ensure that n8n is installed and running in your environment. You can find installation instructions on the [official n8n documentation](https://docs.n8n.io/getting-started/installation/).

2. **Workflow Import**: Import the `Intelligent_Invoicing.json` workflow file into your n8n instance.

3. **Configure Credentials**:
   - Set up the necessary credentials for Postgres, OpenAI, and Google Drive within the n8n Credentials section.
   - Replace the placeholders in the workflow with your actual credentials IDs.

4. **Configure Webhook URLs**:
   - Set up the webhook URLs and ensure they are accessible for receiving POST requests.

5. **Database Setup**:
   - Ensure that your Postgres database is configured and accessible.
   - Create the required tables and schemas as per the workflow's needs.

6. **Google Drive Setup**:
   - Configure the Google Drive node to watch the correct folder for new invoice images.

7. **Test the Workflow**:
   - Execute the workflow manually to test the setup.
   - Check the execution results and logs for any errors and ensure that the workflow completes successfully.

8. **Activate the Workflow**:
   - Once you have confirmed that the workflow is set up correctly and is running as expected, activate it to run automatically.

## Notes

- Make sure to review and test each node's functionality and settings according to your specific use case.
- Adjust the workflow and settings as needed to fit your environment and data structure.
- Regularly check the workflow execution logs to monitor for any issues or errors.

## Support

For support with this workflow, please reach out to the n8n community forum or the support channels provided by the individual service providers (Postgres, OpenAI, Google Drive).