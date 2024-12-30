# Content-summarizer

Overview
The Content Summarizer is a Python application that allows users to input a block of text and receive a concise summary generated using a state-of-the-art Hugging Face Transformer model. The original text and the summary are saved in a local SQLite database, along with the timestamp when the summary was created. Users can view all the previously saved summaries from the database at any time.

Features
Text Summarization: Utilizes the Hugging Face Transformers pipeline to summarize text input by the user.
SQLite Database: Stores original text, summaries, and timestamps for easy retrieval and review.
Simple CLI Interface: A user-friendly command-line interface with options to summarize text, view saved summaries, and exit the program.
Requirements
Python 3.x
transformers library
sqlite3 library (built-in with Python)
You can install the required dependencies using pip:

bash
Copy code
pip install transformers
File Structure
summarizer.py: Main Python script containing the functionality for text summarization, database handling, and user interaction.
summaries.db: SQLite database file where summaries and their timestamps are stored.
Functions
initialize_database()
Initializes the SQLite database and creates a table named summaries to store the original text, summary, and timestamp.

save_to_database(original_text, summary)
Saves the original text, summary, and timestamp into the database.

summarize_text(text)
Summarizes the given input text using the Hugging Face Transformers pipeline. Returns the summary if successful, or None if there was an error.

get_all_summaries()
Retrieves all the summaries from the database, returning them as a list of tuples.

main()
The main program loop that provides the user with the following options:

Summarize text
View saved summaries
Exit the program
How to Use
Clone this repository or download the summarizer.py file.

Install the required libraries using the command:

bash
Copy code
pip install transformers
Run the summarizer.py file:

bash
Copy code
python summarizer.py
Follow the on-screen prompts:

Option 1: Summarize text – Input any text, and the program will return a summary.
Option 2: View saved summaries – Display all summaries stored in the database.
Option 3: Exit the program – Exit the application.
Example Usage
Example 1: Summarizing Text
vbnet
Copy code
Welcome to the Content Summarizer!

Options:
1. Summarize text
2. View saved summaries
3. Exit
Enter your choice: 1
Enter the text to summarize: Content summarization is the process of reducing a text to its essential ideas, while maintaining its original meaning.
Summary:
Content summarization reduces a text to its key ideas while keeping its meaning.
Summary saved to database.
Example 2: Viewing Saved Summaries
vbnet
Copy code
Options:
1. Summarize text
2. View saved summaries
3. Exit
Enter your choice: 2
ID: 1
Original Text: Content summarization is the process of reducing a text to its essential ideas, while maintaining its original meaning.
Summary: Content summarization reduces a text to its key ideas while keeping its meaning.

