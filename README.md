# messagetrace_last90days_M365
# Message Trace for last 90 days in M365
Connect-ExchangeOnline

Import-Csv  -Path "D:\Send_Message_Trace.csv" |
foreach {Start-HistoricalSearch -ReportTitle Send_Trace_Status -StartDate 07/10/2023 -EndDate 10/06/2023 -ReportType MessageTrace -RecipientAddress $_.Email -NotifyAddress ammar.m@contoso.com}


#Check your M365 Admin Center > Message Trace Report > Downloadable File.
