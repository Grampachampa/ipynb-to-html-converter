# .ipynb to .html converter
The converter will go over the folders in the directory one by one, and convert the .ipynb files in each folder to .html. You will need nbconvert installed. Here are the steps to use this thing:

## USAGE
### 1) git clone this repo into the directory that you want to use it in. 📝
It should look like the picture below:<br>
![Alt text](image-2.png)<br>
**It doesn't matter if the .ipynb files are in folders, or what they are called unless id_mode = "FILE".**

### 2) Open "RUN THIS ONE.ipynb", set your settings, and run the file. 🚀
Open the file "RUN THIS ONE.ipynb". Then, just read through it, and run the cells in order, and change the required params in the last cell. The ones you HAVE to change are in the file, but below you can see the optional ones to change:
## Reqired Params (for sending emails)
### ta_name
Your name - used in the email as "Sincerely, yourname".
### ta_email
The address that emails will be sent from
### ta_email_password
Password to ta_email
### assignment_number
assignment number - should be formatted as "Assignment 2" or "Midterm"

## Optional Params
### dir_path
The path of the directory to convert the files in (optional). Default is the current directory. You shouldn't change this.
### file_convert
Whether or not to convert ipynb files to html. Default is True. I wouldn't turn this off, since already-converted files are not converted twice regardless.
### send_email
Whether or not to send the emails. Default is True.
### test_mode
Whether or not to run in test mode. Default is False. -> When True, only converts the first file and sends it to yourself to ensure that everything works as intended.
### go_to_vunet_id
The vunet id to start at. Default is None, which starts at the first folder in the parent directory. Use if the cell crashes mid-run to start from a certain vunet id. This avoids sending emails twice.

### id_mode
"SCRAPE" for scraping from the file (students can and WILL find ways to make this break, believe me)

"FILE" for file path

## Final Notes/Quirks
Due to the way that outlook handles automated emails (i.e. poorly), you Cc yourself in every sent email. This is the only way that I have found to actually be able to see the sent emails, for whatever reason. If this annoys you (it will), I recommend setting up a separate folder in outlook that automatically collects any emails sent by you that have "Feedback and Results" in the subject.