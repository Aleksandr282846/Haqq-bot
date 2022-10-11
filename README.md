# Haqq-bot![12345](https://user-images.githubusercontent.com/45524333/195110103-6f158bf5-1be6-464a-91e1-47e7a28c255f.png)


This small utility can be useful if you want to receive information about the status of the validator in Telegram without depending on third-party services.

The script is installed on the machine with the node and allows you to receive telegram notifications about the following events:


Validator being jailed
Exit from prison
Missed Blocks
New online voting
Small amount of free RAM on the node
Running out of disk space
other notifications (relevant information will be on haqqwatcher.online)

When a notification is received, the message contains a hint for how to react to the event (for example, how to vote or a command to unjail), which can be useful if only a phone is at hand.

Notification examples:

✅ HAQQ WATCHER info ✅ [MaxBoot] unjailed!
  [195.52.40.128]
  haqqvaloper1dkumjqxlgh3al23kg76k5yen9504exxjjwpqne

⚠️ HAQQ WATCHER info ⚠️ [MaxBoot] Low disk space!
  Only 10[G] free.
  
  Your telegram bot (namely chat id and token)
Address of your validator (haqqd keys show wallet --bech val -a or just copy from explorer)

cd
wget -O hw_install.sh https://github.com/Aleksandr282846/HaqqWatcher/raw/main/hw_install.sh && chmod +x ./hw_install.sh && ./hw_install.sh

The installer will ask for the validator address and telegram bot details. After receiving the test message, the script will run as a service, checking the parameters every 15 seconds. To view the logs, enter the command:

journalctl -u haqqwatcher -f -o cat

This completes the installation.


To stop notifications, just stop the service:

systemctl stop haqqwatcher

THAT'S IT!!!!
