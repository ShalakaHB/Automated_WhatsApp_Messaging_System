# Automated_WhatsApp_Messaging_System

![image](https://github.com/user-attachments/assets/d4ae53e7-b739-44f8-bb6c-335ed35fbb6f)

- The project aims to develop an automated system for sending personalized WhatsApp messages to a list of recipients using Python.
- The system will allow the user to upload an Excel file containing contact details or optionally store contact information in a database through a form.
- A text file will be used for message templates.
- Each message will be dynamically personalized based on the recipient’s name and sent.

## Objectives:
1. The primary objectives of this project are:
2. Automate the process of sending WhatsApp messages.
3. Personalize messages using a template-based approach.
4. Validate phone numbers before sending messages.
5. Handle errors gracefully and ensure messages are sent efficiently.
6. Introduce a delay between messages to prevent system overload.
7. Provide two implementation options: one using an Excel file and another using a database for contact management.

## Key Features:
1. Automated Message Dispatch:
The system will read contact information from an Excel sheet or a database (if implemented).
Messages will be sent automatically with placeholders for recipient-specific data (like names).

2. Two Implementation Options:
Excel-Based Approach: Contacts are managed via an Excel file, making it simple to update and modify.
Database-Based Approach: Contacts are stored in a database through a form, ensuring messages are only sent to new entries.

3. Message Personalization:
- A text file will be used as a message template.
Each message will be personalized using the recipient’s name before dispatch.

4. Phone Number Validation:
Basic validation of phone numbers will be implemented (e.g., ensuring that the number has 10 digits for Indian numbers).

5. Error Handling:
Error messages will be logged in case of failed message dispatch due to incorrect phone numbers or connection issues.

6. Delay Between Messages:
A delay of a few seconds between each message ensures that the system doesn't overload or get flagged for sending messages too quickly.

## System Design:
1. Input:
- Excel File (Option 1): Contains two columns: one for names and another for WhatsApp numbers.
- Database Entry (Option 2): Contacts can be added through a form, and the system will process new contacts sequentially.
- Text File: Contains the message template with placeholders for personalization.

2. Output:
- WhatsApp messages are sent to a list of contacts.

3. Workflow:
- Read contact information from an Excel sheet or database (based on the chosen approach).
- Read the message from the text file and personalize it for each recipient.
- Validate the phone numbers.
- Send the message via WhatsApp using pywhatkit.
- Log errors if any message dispatch fails.
- Ensure that newly added database entries are processed first (if using the database approach).

## Tools and Libraries:
- Programming Language: Python

## Libraries:
- pywhatkit: For sending WhatsApp messages.
- pandas: For reading and processing Excel files.
- time: For adding a delay between message sends.
- re: For validating phone numbers.
- sqlite3 or other database connectors (optional for database implementation).

## Technical Requirements:

### Software:
- Python 3.x
- WhatsApp Web (for sending messages)
- Excel file with correct formatting
- Message template text file
- Database setup (optional: SQLite/MySQL/etc.)

### Python Dependencies:
- pywhatkit: For integrating with WhatsApp Web.
- pandas: For Excel file handling.
- re: For validating phone numbers.
- sqlite3 or other database modules (optional for database implementation).

## Project Scope:

### Initial Phase:
- Implement the basic system to read contact details from an Excel file and send personalized WhatsApp messages.

### Validation and Error Handling:

- Add phone number validation to ensure messages are only sent to valid numbers.
- Implement error handling for connection issues or incorrect data.
- Database Integration & Optimization (Optional):
- Implement a form to add contacts dynamically.
- Ensure messages are sent only to the newest entries.
- Optimize the delay between messages to balance system performance and avoid potential rate limiting.

## Limitations:

### WhatsApp Web Limitations:
- pywhatkit relies on WhatsApp Web, which may restrict how many messages can be sent in quick succession.

### Phone Number Formats:
- Incorrect or improperly formatted phone numbers can cause failed message attempts.

### Automation Interruption:
- If the WhatsApp Web session expires or disconnects, the automated messaging might halt.

### Large Contact Lists:
- For extensive contact lists, messages may not be sent immediately but instead remain in drafts. The reason for this is unclear, possibly due to WhatsApp’s internal limitations.

## Benefits:
- Efficiency: Automates a repetitive task, saving time.
- Personalization: Allows for personalized messages based on contact information.
- Error Handling: Gracefully handles issues such as incorrect phone numbers or changing the message template.
- Scalability: Adding more contacts to the database or changing the message template can easily scale up.

## Conclusion:
- This project will deliver a functional, automated system to send personalized WhatsApp messages efficiently and reliably. By leveraging Python and libraries like pywhatkit, the solution will enhance communication, save time, and allow for easy scaling as contact lists grow. Users can choose between an Excel-based approach for quick usage or a database-integrated approach for more dynamic automation.
