# Birthday Wisher Project 🎉

This Python project sends personalized birthday wishes via email. When a birthday matches the current date (month and day), the script reads a random letter template, replaces the placeholder with the birthday person's name, and sends the email to them automatically.

## Features
- Reads birthday data from a CSV file (`birthdays.csv`).
- Randomly selects one of the available birthday letter templates from the `letter_templates` folder.
- Sends a customized birthday email via SMTP.

## How It Works

1. **Fetches Today's Date**: The script identifies today's date using Python's `datetime` module.
2. **Reads Birthday Data**: The `birthdays.csv` file contains names, email addresses, and the birthday dates. The script checks if today's date matches any birthdays in the file.
3. **Customizes a Template**: If a birthday is found, a random birthday letter from `letter_templates/` is chosen. The `[NAME]` placeholder in the letter is replaced with the actual name of the birthday person.
4. **Sends an Email**: The script logs into your email account and sends the customized letter to the birthday person's email address.

## Project Setup

### Prerequisites
1. **Python**: Ensure Python is installed on your machine.
2. **Email Provider Settings**: You'll need access to an email account that allows you to send emails programmatically. For Gmail:
   - Allow less secure apps or use an app-specific password if 2FA is enabled.

### Project Files

1. **`birthdays.csv`**: A CSV file containing birthday data. The file should include columns for `name`, `email`, `year`, `month`, and `day`:
   ```csv
   name,email,year,month,day
   John Doe,johndoe@example.com,1990,9,18
   Jane Smith,janesmith@example.com,1995,9,18

2. **letter_templates/:** Folder containing pre-written birthday letter templates with the `[NAME]` placeholder. Each template should be named as `letter_1.txt`, `letter_2.txt`, etc. Example content:

    ```
    Dear [NAME],

    Wishing you a fantastic birthday! Hope this year brings you great joy.

    Best,
    Your Friend

3. **Python Script:** The Python script sends the email based on the current date and the data in `birthdays.csv`.


### Required Changes
To run the code, update the following four places:

1. **Email Credentials:** Replace `MY_EMAIL` and `MY_PASSWORD` with your email and password in the script:
    ```
    MY_EMAIL = "your-email@example.com"
    MY_PASSWORD = "your-email-password"

2. **Email Provider Setting:** Allow less secure apps on your email account (depending on your provider) or generate an app-specific password if using Gmail with 2FA.

3. **SMTP Server Address:** Replace "YOUR EMAIL PROVIDER SMTP SERVER ADDRESS" with your email provider's SMTP server. Example for Gmail:
    ```
    smtp.gmail.com

4. **Birthday Data:** Ensure that the birthdays.csv file contains today's date (month and day) for at least one person.


### Installation & Usage
1. **Clone the repository:**
    ```
    git clone https://github.com/your-username/birthday-wisher.git

2. **Install dependencies:**
    ```
    pip install pandas

3. **Run the script:**
    ```
    python main.py

If a birthday matches today's date, the script will send the birthday wish automatically!


### Example Workflow
1. The script checks if today (e.g., September 18) matches any birthday in `birthdays.csv`.
2. It randomly picks one of the `letter_templates` (e.g., `letter_2.txt`).
3. It replaces the `[NAME]` placeholder with the person's name.
4. Finally, it sends the email using the specified SMTP server.


### Credits
This project is part of the 100 Days of Python course.
