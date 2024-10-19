# Microsoft 365 group
Microsoft 365 Groups are used for collaboration between users, both inside and outside your company. With each Microsoft 365 group, members get a group email and shared workspace for conversations, files, and calendar events, as well as Stream and a Planner. Microsoft 365 Groups can also be connected to Teams or Viva Engage. Learn more about Microsoft 365 group from [Microsoft's documentation](https://learn.microsoft.com/en-us/microsoft-365/admin/create-groups/compare-groups?view=o365-worldwide#microsoft-365-groups).

# About the script
The [add-members-to-M365group](add-members-to-M365group.ps1) will help engineers and administrators to add multiple users to a 365 group. 
## Script breakdown
1. It will import the [ExchangeOnlineManagement](https://learn.microsoft.com/en-us/powershell/exchange/exchange-online-powershell-v2?view=exchange-ps) REST API module
2. Uses the [Connect-ExchangeOnline](https://learn.microsoft.com/en-us/powershell/module/exchange/connect-exchangeonline?view=exchange-ps) method to connect to your EAC
3. Uses the [Import-Csv](https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/import-csv?view=powershell-7.4) cmdlet to import a CSV file that contains the UPN or email address of the members.
4. Then, use the For Loop to review the CSV file and add each member.
