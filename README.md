### Telegram Bot for Points Calculation

This Telegram bot is designed to count the number of characters in user messages in chats and assign points based on the length of these messages. Only the bot owner has the rights to use special commands to manage the bot.

Functionality

Points Calculation

The bot calculates points for each user message based on the following logic:

	•	If the message contains up to 10 characters: The user earns 0.25 points per character.
	•	If the message contains between 10 and 25 characters: The user earns 0.5 points per character.
	•	If the message contains between 25 and 75 characters: The user earns 0.75 points per character.
	•	If the message contains more than 75 characters: The user earns 1 point per character.

Leaderboard Management

The bot tracks the points earned by users in each chat and generates a leaderboard based on these data. The bot owner can view the current top 10 users using a special command.

Commands

	•	/start: Starts the bot and notifies that the bot begins tracking points.
	•	/reset: Resets all tracking data in the current chat. This command can only be used by the bot owner.
	•	/top: Shows the current top 10 users with the highest points in the chat. This command can only be used by the bot owner.
	•	/getfile: Sends an Excel file with all points tracking data in the current chat. This command can only be used by the bot owner.

Data Storage

The bot saves user points data in an Excel file, which is updated every minute. This file contains the following information:

	•	Chat ID
	•	User ID
	•	Username
	•	Number of points earned

Automated Messages

The bot automatically sends a summary message of the top 10 users weekly and resets the points counters after sending this message.

Requirements

	•	.NET 5.0 or newer
	•	Telegram Bot API
	•	Telegram.Bot library
	•	EPPlus library for working with Excel

How to Run

	1.	Clone this repository.
	2.	Install the required packages via NuGet:
	•	Telegram.Bot
	•	OfficeOpenXml
	3.	Change botOwnerId in the code to your Telegram ID.
	4.	Run the project using Visual Studio or the command line.

Contribution

You can contribute by creating pull requests or reporting issues in the issues section. Your suggestions for improving the bot’s functionality are welcome.
