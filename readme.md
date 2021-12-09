[comment]: # "Auto-generated SOAR connector documentation"
# ClickSend

Publisher: Han Lievens  
Connector Version: 1\.0\.4  
Product Vendor: ClickSend  
Product Name: ClickSend  
Product Version Supported (regex): "\.\*"  
Minimum Product Version: 3\.0\.251  

This app integrates with ClickSend to send SMS messages


You can find the API credentials in your account area under 'API Credentials' at the top of the
screen.


### Configuration Variables
The below configuration variables are required for this Connector to operate.  These variables are specified when configuring a ClickSend asset in SOAR.

VARIABLE | REQUIRED | TYPE | DESCRIPTION
-------- | -------- | ---- | -----------
**base\_url** |  required  | string | The API should always be accessed over SSL
**username** |  required  | string | Username Example\: myusername
**key** |  required  | password | API Key
**to** |  optional  | string | Recipient Mobile Number \(used only for Test Connectivity\)

### Supported Actions  
[test connectivity](#action-test-connectivity) - Validate the asset configuration for connectivity  
[send message](#action-send-message) - Send an SMS Text  

## action: 'test connectivity'
Validate the asset configuration for connectivity

Type: **test**  
Read only: **True**

#### Action Parameters
No parameters are required for this action

#### Action Output
No Output  

## action: 'send message'
Send an SMS Text

Type: **generic**  
Read only: **False**

You can post up to 1000 messages with each API call\. You can send to a mix of contacts and contact lists, as long as the total number of recipients is up to 1000\. The response contains a status and details for each recipient\.

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**to** |  required  | Recipient Phone Number\. If country code not specified will default to \+1 | string |  `phone number` 
**message** |  required  | The message to be sent\. Maximum 960 characters\. Example\: This is a test | string | 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.parameter\.to | string |  `phone number` 
action\_result\.parameter\.message | string | 
action\_result\.status | string | 
action\_result\.message | string | 
summary\.total\_objects | numeric | 
summary\.total\_objects\_successful | numeric | 
action\_result\.data\.\*\.response\_code | string | 
action\_result\.data\.\*\.data\.total\_count | numeric | 
action\_result\.data\.\*\.data\.\_currency\.currency\_prefix\_d | string | 
action\_result\.data\.\*\.data\.\_currency\.currency\_name\_long | string | 
action\_result\.data\.\*\.data\.\_currency\.currency\_name\_short | string | 
action\_result\.data\.\*\.data\.\_currency\.currency\_prefix\_c | string | 
action\_result\.data\.\*\.data\.messages\.\*\.body | string | 
action\_result\.data\.\*\.data\.messages\.\*\.status | string | 
action\_result\.data\.\*\.data\.messages\.\*\.direction | string | 
action\_result\.data\.\*\.data\.messages\.\*\.message\_parts | numeric | 
action\_result\.data\.\*\.data\.messages\.\*\.from | string | 
action\_result\.data\.\*\.data\.messages\.\*\.schedule | numeric | 
action\_result\.data\.\*\.data\.messages\.\*\.country | string | 
action\_result\.data\.\*\.data\.messages\.\*\.custom\_string | string | 
action\_result\.data\.\*\.data\.messages\.\*\.contact\_id | string | 
action\_result\.data\.\*\.data\.messages\.\*\.from\_email | string | 
action\_result\.data\.\*\.data\.messages\.\*\.to | string | 
action\_result\.data\.\*\.data\.messages\.\*\.carrier | string | 
action\_result\.data\.\*\.data\.messages\.\*\.subaccount\_id | numeric | 
action\_result\.data\.\*\.data\.messages\.\*\.list\_id | string | 
action\_result\.data\.\*\.data\.messages\.\*\.date | numeric | 
action\_result\.data\.\*\.data\.messages\.\*\.user\_id | numeric | 
action\_result\.data\.\*\.data\.messages\.\*\.message\_price | string | 
action\_result\.data\.\*\.data\.messages\.\*\.message\_id | string | 
action\_result\.data\.\*\.data\.total\_price | numeric | 
action\_result\.data\.\*\.data\.queued\_count | numeric | 
action\_result\.data\.\*\.http\_code | numeric | 
action\_result\.data\.\*\.response\_msg | string | 
action\_result\.summary\.response\_message | string | 