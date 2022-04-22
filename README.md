# Monitor-AAD-App-Secrets-Expiration
Power Automate flow to get notified when an Azure AD App Secret expires soon

This Power Automate flow helps to get notified with the list of Azure AD Application Secrets that expire soon.

It leverage Graph API to check, from a daily basis, AAD Secrets that expire in a certain interval.
Time interval to monitor is fully configurable.

![image](https://user-images.githubusercontent.com/22662809/164730035-af827719-5c5a-40f2-b5b6-0e8dc9a2bdf4.png)

## Installation

1.  Download the included Zip file.
2.  Go to make.powerapps.com 
3.  Click on the Solutions tab
4.  Select the "Import Solution" button
5.  Run through the set up _(refer to [Configuration](#configuration))_
6.  Your solution is ready to use!

## Configuration

| Name | Type | Description |
|---|---|---|
| ADDSecrets-Http with Azure AD | Connection Reference | Connection to query Graph API.<br />Use _https://graph.microsoft.com/_ for _Base Resource URL_ & _Azure AD Resource URI_ fields |
| ADDSecrets-Outlook | Connection Reference | Outlook account used to send email |
| ADDSecrets-Recipients  | Environment Variable | Emails to notify separated by semicolumn |
| ADDSecrets-TimeInterval-Value | Environment Variable | Time interval to monitor _(Default: 1)_|
| ADDSecrets-TimeInterval-Unit | Environment Variable | Unit of time interval to monitor _(Default: Month)_ |
