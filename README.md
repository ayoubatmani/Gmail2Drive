# Gmail2Drive
Google Script to Save Gmail attachements to Google Drive

Introduction
This script will look for attachments in Gmail Message and Extract it to a Google Drive folder. Script can be run manually or through a time driven trigger. The script can be personalized by following the instructions
 given in this article.
 
 Installation notes
Make a copy of this script project
In the new copy of the script, go to Resources > Current Project’s triggers 
Click on the link displayed to setup a time driven trigger and save the trigger. Frequency depends on how frequently you want to look for new messages in Gmail. Here is a screenshot of the trigger settings to run every minute.

Click on notifications and choose your notification preferences. This will notify you if there occurs execution failure. Here is an screenshot of the notification preferences

If you are running the script first time, it will ask you to authorize the script for “Gmail” and “Google Drive” access. Authorize it. Now the script installation is complete.
This procedure can be followed with any Gmail account. Once the installation is complete, script will run as per the specified interval, look for messages in Gmail which are not labelled and have attachments as file types specified. It will extract the attachment to a Google Drive folder and label the Gmail Message 'GmailToDrive'.
Would you like to set your preferences?
You may change line 3, 5 and 7 as per your preferences.


var fileTypesToExtract = ['jpg', 'tif', 'png', 'gif', 'bmp', 'svg'];
This is an array for file types to look for. You may add or remove file types from this array.

var folderName = 'GmailToDrive';
This is the name of the folder to which files will be extracted to in Google Drive. If the script does not finds a folder with this name, it will create the folder in drive.

var labelName = 'GmailToDrive';
This label name is Gmail Label name. This is used by the script to identify which message has been processed and which has not not. Once a message is processed, script will put a label on those messages with below name. You may change the label name too.
