
|SIEM USE CASEs configuration and compliance document|
| :- |
|Baselining the systems against SOC operational requirements|
|IS Ops team|

**TABLE OF CONTENTS**

[**1. BACKGROUND	6****]()

[**2. SCOPE	6****]()

[**3. RESPONSIBILITY	6****]()

[**3.1.**	**SOC team	6****]()

[**3.2.**	**GRC Team	6****]()

[**3.3.**	**Internal Audit	6****]()

[**3.4.**	**Systems / Control owners	6****]()

[**3.5.**	**Management	7****]()

[**4. USE-CASE DEFINITION AND ATTRIBUTES	7****]()

[**4.1.**	**Section ID: Application	7****]()

[**4.1.1. Sub-section ID: Inside Attack	7****]()

[4.1.1.1. Reference ID: 1.3.1.1.	7]()

[4.1.1.1.1. Goal	7]()

[4.1.1.1.2. Sources	7]()

[4.1.1.1.3. Requirements	7]()

[4.1.1.1.4. Troubleshooting steps	10]()

[4.1.1.1.5. Event to ID mapping	12]()

[4.1.1.1.6. Dependency	12]()

[4.1.1.1.7. Affected Area	12]()

[4.1.1.1.8. Limitations	12]()

[4.1.1.1.9. References	12]()

[4.1.1.2. Reference ID: 1.3.1.2	12]()

[4.1.1.2.1. Goal	12]()

[4.1.1.2.2. Sources	12]()

[4.1.1.2.3. Requirements	13]()

[4.1.1.2.4. Event to ID mapping	13]()

[4.1.1.2.5. Troubleshooting steps	13]()

[4.1.1.2.6. Dependency	13]()

[4.1.1.2.7. Limitations	13]()

[4.1.1.2.8. Affected area	13]()

[4.1.1.2.9. References	13]()

[**4.1.2. Sub-section ID: External Attack	14****]()

[4.1.2.1. Reference ID: 1.3.2.1	14]()

[4.1.2.1.1. Goal	14]()

[4.1.2.1.2. Sources	14]()

[4.1.2.1.3. Requirements	14]()

[4.1.2.1.4. Event to ID mapping	14]()

[4.1.2.1.5. Troubleshooting steps	14]()

[4.1.2.1.6. Dependency	14]()

[4.1.2.1.7. Limitations	15]()

[4.1.2.1.8. Affected Area	15]()

[4.1.2.1.9. References	15]()

[**4.1.3. Sub-section ID: Visibility	15****]()

[4.1.3.1. Reference ID: 1.3.3.1	15]()

[4.1.3.1.1. Goal	15]()

[4.1.3.1.2. Sources	15]()

[4.1.3.1.3. Requirements	15]()

[4.1.3.1.4. Audit to Event-ID mapping	16]()

[4.1.3.1.5. Limitations	16]()

[4.1.3.1.6. Troubleshooting steps	16]()

[4.1.3.1.7. Dependency	16]()

[4.1.3.1.8. Affected Area	16]()

[4.1.3.1.9. References	16]()

[4.1.3.2. Reference ID: 1.3.3.2	16]()

[4.1.3.2.1. Goal	16]()

[4.1.3.2.2. Sources	16]()

[4.1.3.2.3. Requirements	16]()

[4.1.3.2.4. Event to Audit ID Mapping	17]()

[4.1.3.2.5. Troubleshooting	18]()

[4.1.3.2.6. Dependency	18]()

[4.1.3.2.7. Limitations	18]()

[4.1.3.2.8. Affected Area	18]()

[4.1.3.2.9. References	18]()

[4.1.3.3. Reference ID: 1.3.3.3	18]()

[4.1.3.3.1. Goal	18]()

[4.1.3.3.2. Sources	18]()

[4.1.3.3.3. Requirements	18]()

[4.1.3.3.4. Troubleshooting	18]()

[4.1.3.3.5. Auditing to Event-ID Mapping	19]()

[4.1.3.3.6. Dependency	19]()

[4.1.3.3.7. Limitations	19]()

[4.1.3.3.8. Affected Area	19]()

[4.1.3.3.9. References	19]()

[4.1.3.4. Reference ID: 1.3.3.4	19]()

<a name="_hlt349891569"></a><a name="_hlt349891570"></a>[4.1.3.4.1. Goal	19]()

[4.1.3.5. Reference ID: 1.3.3.5	19]()

[4.1.3.5.1. Goal	19]()

[4.1.3.5.2. Sources	19]()

[4.1.3.5.3. Requirements	19]()

[4.1.3.5.4. Audit to Event-ID mapping	20]()

[4.1.3.5.5. Troubleshooting	20]()

[4.1.3.5.6. Dependency	20]()

[4.1.3.5.7. Limitations	20]()

[4.1.3.5.8. Affected Area	20]()

[4.1.3.5.9. References	20]()

[4.1.3.6. Reference ID: 1.3.3.6	20]()

[4.1.3.6.1. Goal	20]()

[4.1.3.6.2. Sources	20]()

[4.1.3.6.3. Requirements	20]()

[4.1.3.6.4. Event to audit Mapping	21]()

[4.1.3.6.5. Troubleshooting	21]()

[4.1.3.6.6. Dependency	21]()

[4.1.3.6.7. Affected Area	21]()

[4.1.3.6.8. Limitations	21]()

[4.1.3.6.9. References	21]()

[4.1.3.7. Reference ID: 1.3.3.7	21]()

[4.1.3.7.1. Goal	21]()

[4.1.3.7.2. Sources	21]()

[4.1.3.7.3. Requirements	21]()

[4.1.3.7.4. Troubleshooting	22]()

[4.1.3.7.5. Dependency	22]()

[4.1.3.7.6. Limitations	22]()

[4.1.3.7.7. Affected Area	22]()

[4.1.3.7.8. References	22]()

[**4.1.4. Sub-section ID: Policy violations	22****]()

[4.1.4.1. Reference ID: 1.3.4.1	22]()

[4.1.4.1.1. Goal	22]()

[4.1.4.1.2. Sources	23]()

[4.1.4.1.3. Requirements	23]()

[4.1.4.1.4. Troubleshooting	24]()

[4.1.4.1.5. Limitations	24]()

[4.1.4.1.6. Dependency	24]()

[4.1.4.1.7. Affected Area	24]()

[4.1.4.1.8. References	24]()

[4.1.4.2. Reference ID: 1.3.4.2	24]()

[4.1.4.2.1. Goal	24]()

[4.1.4.2.2. Sources	24]()

[4.1.4.2.3. Requirements	24]()

[4.1.4.2.4. Audit to Event Id mapping	25]()

[4.1.4.2.5. Troubleshooting	25]()

[4.1.4.2.6. Dependency	25]()

[4.1.4.2.7. Limitations	25]()

[4.1.4.2.8. Affected Area	25]()

[4.1.4.2.9. References	26]()

[4.1.4.3. Reference ID: 1.3.4.2	26]()

[4.1.4.3.1. Goal	26]()

[4.1.4.3.2. Sources	26]()

[4.1.4.3.3. Requirements	26]()

[4.1.4.3.4. Audit to Event Id mapping	27]()

[4.1.4.3.5. Troubleshooting	27]()

[4.1.4.3.6. Affected Area	27]()

[4.1.4.3.7. Dependency	28]()

[4.1.4.3.8. Limitations	28]()

[4.1.4.3.9. References	28]()

[**4.1.5. Sub-section ID: Legal	28****]()

[4.1.5.1. Reference ID: 1.3.5.1	28]()

[4.1.5.1.1. Goal	28]()

[4.1.5.1.2. Sources	28]()

[4.1.5.1.3. Requirements	28]()

[4.1.5.1.4. Audit to Event Id mapping	28]()

[4.1.5.1.5. Troubleshooting	28]()

[4.1.5.1.6. Limitations	28]()

[4.1.5.1.7. Dependency	29]()

[4.1.5.1.8. Affected Area	29]()

[4.1.5.1.9. References	29]()



**Document Information**

|**Document Title**|**Incident Response Policy**|
| :- | :- |
|**Drafted by**|NADRA IS Operations team|
|**Draft Date**|Jan 5, 2013|
|**Owner**|NADRA|
|**Classification/ Classification Authority**|Internal / NADRA|
|**Release Version**|1\.1|
|**Reference document** |SOC implementation plan|
|**Approval Date**||
|**Approved By**||
|**Published Date**||
#





1. # <a name="_toc348891529"></a>**<a name="_toc348891530"></a><a name="_toc349891424"></a>Background**
The purpose of this document is to illustrate assets owners the underlying procedural requirements and configurations necessary to operate and sustain SOC operations. The understanding of these requirements by owners is critically important in determining the success of SOC operations, In case of any change resulting due to improper configuration or management of these requirements can directly impact the performance of SOC operations team in timely detection and response to security incidents.
1. # <a name="_toc348891531"></a><a name="_toc349891425"></a>**Scope**
The scope of this exercise stretches within the bounds of use-cases requirements mentioned in the SOC implementation plan referenced above (Document Information).
1. # <a name="_toc348891532"></a><a name="_toc349891426"></a>**Responsibility** 
   1. ## <a name="_toc348891533"></a><a name="_toc349891427"></a>**SOC team** 
The team is responsible for:-

- Maintaining an auditable trail to prove events of interest were followed up on and resolved.
- Active monitoring of controls

  1. ## ` `**<a name="_toc348891534"></a><a name="_toc349891428"></a>GRC Team**
The team is responsible to update, maintain policies for relevancy and to reflect the configuration requirements herein mentioned.
1. ## ` `**<a name="_toc348891535"></a><a name="_toc349891429"></a>Internal Audit** 
The audit is responsible for:-

- Reviewing the internal controls, periodically or as mentioned in annual audit plan or as directed by the regulator, implemented by senior management. 
- Internal auditors will evaluate and review the internal controls in place and report for its improvements. 
- To ensure that SOPs are followed by concerned department and grey areas, if any, are identified with recommendations how to counter the same.
  1. ## ` `**<a name="_toc348891536"></a><a name="_toc349891430"></a>Systems / Control owners** 
The owners are responsible for:-

- Introducing internal Controls through SOPs which are prepared in consultation with respective departmental heads, reviewed and approved by management for implementing the same.
- Configuration and management of audit rules as per policies (e.g Change and configuration management policy).
  1. ## ` `**<a name="_toc348891537"></a><a name="_toc349891431"></a>Management**
The management is responsible for:-

- Establishing a mechanism to update the audit procedures.
- Establishing a periodic review of audit activities and to adjust those audit activities to better support the NADRA’s business goals
1. # <a name="_toc348891538"></a><a name="_toc349891432"></a>**Use-Case definition and Attributes**
   1. ## <a name="_toc348891539"></a><a name="_toc349891433"></a>**Section ID: Application**
      1. ### <a name="_toc348891540"></a><a name="_toc349891434"></a>**Sub-section ID: Inside Attack**
         1. #### <a name="_toc348891541"></a><a name="_toc349891435"></a>**Reference ID: 1.3.1.1.**
            1. ##### <a name="_toc348891542"></a><a name="_toc349891436"></a>**Goal**
Under this use-case the SOC operations team would be abnormal traffic pattern in non-business hours
1. ##### ` `**<a name="_toc348891543"></a><a name="_toc349891437"></a>Sources**
Web Server, HIDS, Q-Flow
1. ##### <a name="_toc348891544"></a><a name="_toc349891438"></a>**Requirements**
1. Web Server [1]
- Apache logs collection

Monitoring a log file

1. **Make changes in  /var/ossec/etc/ossec.conf**

<ossec\_config>

`  `<localfile>

`    `<log\_format>apache</log\_format>

`    `<location>/var/log/apache/access\_log</location>

`  `</localfile>

</ossec\_config

1. IIS server [2]
1. By default, the installation scripts will attempt to configure OSSEC to monitor the first virtual hosts for web (W3SVC1 to W3SVC254), ftp (MSFTPSVC1 to MSFTPSVC254) and smtp (SMTPSVC1 to SMTPSVC254)





![](Aspose.Words.74e725a8-9807-4d94-8b20-a5fea5e2882c.001.png)![](Aspose.Words.74e725a8-9807-4d94-8b20-a5fea5e2882c.002.jpeg)

#####
#####
#####










![](Aspose.Words.74e725a8-9807-4d94-8b20-a5fea5e2882c.003.jpeg)

























![](Aspose.Words.74e725a8-9807-4d94-8b20-a5fea5e2882c.004.jpeg)


















<localfile>

`    `<location>%WinDir%\System32\LogFiles\W3SVC3\ex%y%m%d.log</location>

`    `<log\_format>iis</log\_format>

</localfile>





















1. ##### <a name="_toc348891545"></a><a name="_toc349891439"></a>**Troubleshooting steps**
































1. ![](Aspose.Words.74e725a8-9807-4d94-8b20-a5fea5e2882c.005.png)**Enable debug mode**


















If this is on an OSSEC server you can enable debug by running:




![](Aspose.Words.74e725a8-9807-4d94-8b20-a5fea5e2882c.006.png)


Enable debug mode and restart the OSSEC processes to view more verbose logs.

There is a firewall between the agent and the server.









![](Aspose.Words.74e725a8-9807-4d94-8b20-a5fea5e2882c.007.png)




1. **Wrong authentication keys configured (you imported a key from a different agent).**


If that’s the case, you would be getting logs similar to the above on the agent and the following on the server (see also Errors:1403):






![](Aspose.Words.74e725a8-9807-4d94-8b20-a5fea5e2882c.008.png)



1. **Agent won’t connect to the manager or the agent always shows never connected**











![](Aspose.Words.74e725a8-9807-4d94-8b20-a5fea5e2882c.009.png)












**Step by Step – adding the authentication keys**

For most of the errors (except the firewall issue), removing and re-adding the authentication keys fix the problem. Do the following if you are having issues:

1. ‘Stop the server and the agent.’
   1. Make sure they are really stopped (ps on Unix or sc query ossecsvc on Windows)
1. Run the manage-agents tool on the server and remove the agent.
1. Still on the server, add the agent using manage-agents. Make sure the IP is correct.
1. Start the server.
1. Run manage-agents on the agent and import the newly generated key.
1. Start the agent.

If after that, it still doesn’t work, contact our mailing list for help.

For additional information regarding troubleshooting refer to reference section
1. ##### <a name="_toc348891546"></a><a name="_toc349891440"></a>**Event to ID mapping** 
N/A
1. ##### <a name="_toc348891547"></a><a name="_toc349891441"></a>**Dependency** 
N/A
1. ##### <a name="_toc349891442"></a>**Affected Area**
- All NADRA domain machines.
- Critical unix servers
- Core network devices (public facing)

1. ##### <a name="_toc348891548"></a><a name="_toc349891443"></a>**Limitations**
1. The communication between agent and server relies on UDP port 1514 UDP to be open between two ends

1. UAC may be blocking the OSSEC service from communicating with the manager on Windows 
   1. ##### <a name="_toc348891549"></a><a name="_toc349891444"></a>**References** 
[1] <http://devio.us/~ddp/ossec/docs27/ossec101/managing_agents/localfile.html>

[2] <http://www.ossec.net/doc/manual/monitoring/file-log-monitoring.html>

[3] <http://www.ossec.net/doc/faq/unexpected.html>
1. #### <a name="_toc348891550"></a><a name="_toc349891445"></a>**Reference ID: 1.3.1.2**
   1. ##### <a name="_toc348891551"></a><a name="_toc349891446"></a>**Goal**
In this case SOC Operations Team would be detecting if buffer overflow event has taken place.
1. ##### <a name="_toc348891552"></a><a name="_toc349891447"></a>**Sources**
OSSEC, applications logs, firewall




1. ##### <a name="_toc348891553"></a><a name="_toc349891448"></a>**Requirements** 
1. Ossec

Monitor for attack patter related to buffer-overflow (see below section for more details).












![](Aspose.Words.74e725a8-9807-4d94-8b20-a5fea5e2882c.010.png)




1. ##### <a name="_toc348891554"></a><a name="_toc349891449"></a>**Event to ID mapping**

|Details [1]|||
| :- | :- | :- |
|**Product:**|OSSEC||
|**Maps to**|4\.1.2.3.||
|**Rule ID:**|ID|Description |
||40104|Possible buffer overflow attempt|
|**Type**|Buffer attack ||

1. ##### <a name="_toc348891555"></a><a name="_toc349891450"></a>**Troubleshooting steps**
For OSSEC use the troubleshooting steps given in section 4.1.1.1
1. ##### <a name="_toc348891556"></a><a name="_toc349891451"></a>**Dependency**
Use this configuration 4.1.1.1 to setup apache and IIS.
1. ##### <a name="_toc348891557"></a><a name="_toc349891452"></a>**Limitations**
1. The communication between agent and server relies on UDP port 1514 UDP to be open between two ends

1. UAC may be blocking the OSSEC service from communicating with the manager on Windows 

1. ##### <a name="_toc349891453"></a>**Affected area**
All critical applications
1. ##### <a name="_toc348891558"></a><a name="_toc349891454"></a>**References** 
http://www.ossec.net/doc/rules/rules/70\_attack\_rules.xml.html
1. ### <a name="_toc348891559"></a><a name="_toc349891455"></a>**Sub-section ID: External Attack**
   1. #### <a name="_toc348891560"></a><a name="_toc349891456"></a>**Reference ID: 1.3.2.1**
      1. ##### <a name="_toc348891561"></a><a name="_toc349891457"></a>**Goal**
In this case SOC Operations Team would be detecting for directory transversal attack.
1. ##### <a name="_toc348891562"></a><a name="_toc349891458"></a>**Sources**
OSSEC, applications logs, firewall
1. ##### <a name="_toc348891563"></a><a name="_toc349891459"></a>**Requirements** 
1. Webserver 
   1. Apache & IIS

Monitor for attack patter related to directory transversal.























![](Aspose.Words.74e725a8-9807-4d94-8b20-a5fea5e2882c.011.png)





#####
#####
1. ##### <a name="_toc348891564"></a><a name="_toc349891460"></a>**Event to ID mapping**

|Details [1]|||
| :- | :- | :- |
|**Product:**|OSSEC||
|**Maps to**|4\.1.2.3.||
|**Rule ID:**|ID|Description |
||31104|Possible directory transversal attempt|
|**Type**|Buffer attack ||

1. ##### <a name="_toc348891565"></a><a name="_toc349891461"></a>**Troubleshooting steps**
For OSSEC use the troubleshooting steps given in section 4.1.1.1
1. ##### <a name="_toc348891566"></a><a name="_toc349891462"></a>**Dependency**
Use this configuration 4.1.1.1 to setup apache and IIS.
1. ##### <a name="_toc348891567"></a><a name="_toc349891463"></a>**Limitations**
1. The communication between agent and server relies on UDP port 1514 UDP to be open between two ends

1. UAC may be blocking the OSSEC service from communicating with the manager on Windows 

1. ##### <a name="_toc349891464"></a>**Affected Area**
- All NADRA critical applications
  1. ##### <a name="_toc348891568"></a><a name="_toc349891465"></a>**References** 
http://www.ossec.net/doc/rules/rules/50\_web\_rules.xml.html

1. ### <a name="_toc348891569"></a><a name="_toc349891466"></a>**Sub-section ID: Visibility** 
   1. #### <a name="_toc348891570"></a><a name="_toc349891467"></a>**Reference ID: 1.3.3.1**
      1. ##### <a name="_toc348891571"></a><a name="_toc349891468"></a>**Goal**
Under this use-case the SOC operations team would be listing the number of applications user who have been authenticated to application and never to ADSources on a given day.
1. ##### <a name="_toc348891572"></a><a name="_toc349891469"></a>**Sources**
OSSEC, Active directory
1. ##### <a name="_toc348891573"></a><a name="_toc349891470"></a>**Requirements**
Enable apache to log username use this settings

1. **Apache**

   **Start PHP as an Apache module (For PHP)**

   apache\_note( 'username', $username );

In your server configuration make changes to file **mod\_log\_config.c**

LogFormat "%h %l %{username}n %t \"%r\" %>s %b" common\_with\_php\_username

`			          `CustomLog logs/access\_log common\_with\_php\_username

Compare the recent application user login activity with AD user-session information, Fire alarm if a user has not logged in the day.

1. Configure IIS to send attribute cs-username.[2]


1. ##### <a name="_toc348891574"></a><a name="_toc349891471"></a>**Audit to Event-ID mapping** 
N/A
1. ##### <a name="_toc348891575"></a><a name="_toc349891472"></a>**Limitations**
1. The communication between agent and server relies on UDP port 1514 UDP to be open between two ends
1. UAC may be blocking the OSSEC service from communicating with the manager on Windows 
   1. ##### <a name="_toc348891576"></a><a name="_toc349891473"></a>**Troubleshooting steps**
For OSSEC use the troubleshooting steps given in section 4.1.1.1
1. ##### <a name="_toc348891577"></a><a name="_toc349891474"></a>**Dependency** 
N/A 
1. ##### <a name="_toc349891475"></a>**Affected Area**
- All NADRA critical applications.
  1. ##### <a name="_toc348891578"></a><a name="_toc349891476"></a>**References** 
[1] <http://stackoverflow.com/questions/3389169/put-username-in-apache-access-log-with-php-and-without-http-auth>

[2]http://www.microsoft.com/technet/prodtechnol/WindowsServer2003/Library/IIS/676400bc-8969-4aa7-851a-9319490a9bbb.mspx?mfr=true

[2] <http://httpd.apache.org/docs/2.2/mod/mod_log_config.html#customlog>
1. #### <a name="_toc348891579"></a><a name="_toc349891477"></a>**Reference ID: 1.3.3.2**
   1. ##### <a name="_toc348891580"></a><a name="_toc349891478"></a>**Goal**
The use case will allow the SOC team to monitor if the number of times a particular application has crashed on a given day.
1. ##### <a name="_toc348891581"></a><a name="_toc349891479"></a>**Sources**
OSSEC
1. ##### <a name="_toc345668159"></a><a name="_toc348891582"></a><a name="_toc349891480"></a>**Requirements**
1. Webserver

Apache view / get error.log for following messages 

- Apache service started
- SIGTERM, shutting down

RHEL / Red Hat / CentOS / Fedora Linux Apache error file location:-  **/var/log/httpd/error\_log**

Debian / Ubuntu Linux Apache error log file location - **/var/log/apache2/error.log**

FreeBSD Apache error log file location –

**/var/log/httpd-error.log**

IIS view / get error in Application log related to following messages:-

- Faulting application w3wp.exe

`       `To locate IIS logs goto directory 

C:\Windows\System32\LogFiles\W3SVC1
1. ##### <a name="_toc348891583"></a><a name="_toc349891481"></a>**Event to Audit ID Mapping** 

|Details [1]||
| :- | :- |
|**Product:**|Exchange|
|**Maps to**|4\.1.3.2 |
|**Event ID:**|1009|
|**Event Type**|Error|
|**Source:**|W3SVC|
|**Description**|A process serving application pool 'DefaultAppPool' terminated unexpectedly. The process id was '1234'. The process exit code was '0xc0000005'.|













|Details [2]||
| :- | :- |
|**Product:**|Exchange|
|**Maps to**|4\.1.3.2 |
|**Event ID:**|1000|
|**Event Type**|Error|
|**Source:**|W3SVC|
|**Description**|Faulting application w3wp.exe, version 6.0.3790.1830, faulting module <some module name>, version <some numbers with dots>, fault address 0x<some numbers and letters a thru f>.|








1. ##### <a name="_toc348891584"></a><a name="_toc349891482"></a>**Troubleshooting**
<a name="_toc348891585"></a>Use [IIS State](http://www.iisfaq.com/default.aspx?view=P197) or [DebugDiag](http://www.microsoft.com/downloads/details.aspx?familyid=9bfa49bc-376b-4a54-95aa-73c9156706e7&displaylang=en) tools[1]
1. ##### <a name="_toc345668162"></a><a name="_toc348891586"></a><a name="_toc349891483"></a>**Dependency**
N/A
1. ##### <a name="_toc348891587"></a><a name="_toc349891484"></a>**Limitations**
N/A

1. ##### <a name="_toc349891485"></a>**Affected Area**
- All NADRA critical applications.
  1. ##### <a name="_toc345668163"></a><a name="_toc348891588"></a><a name="_toc349891486"></a>**References** 
[1] http://www.microsoft.com/en-us/download/details.aspx?id=26798
1. #### <a name="_toc348891589"></a><a name="_toc349891487"></a>**Reference ID: 1.3.3.3**
   1. ##### <a name="_toc348891590"></a><a name="_toc349891488"></a>**Goal**
This use case allows the SOC team to detect if the user tries to upload suspicious .php file to the web-server.
1. ##### ` `**<a name="_toc348891591"></a><a name="_toc349891489"></a>Sources**
Ossec
1. ##### <a name="_toc348891592"></a><a name="_toc349891490"></a>**Requirements**
Webserver

1. Apache

   Use apache logs to analyze PUT / POST commands with identified extensions

   Change / Append the log common format with attribute (%X)[2]

`				       `LogFormat "%h %X %l %u %t \"%r\" %>s %b" common

1. IIS	

   Same applies as above.
   1. ##### <a name="_toc348891593"></a><a name="_toc349891491"></a>**Troubleshooting**
For OSSEC use the troubleshooting steps given in section 4.1.1.1
1. ##### <a name="_toc348891594"></a><a name="_toc349891492"></a>**Auditing to Event-ID Mapping**
N/A
1. ##### <a name="_toc348891595"></a><a name="_toc349891493"></a>**Dependency**
N/A
1. ##### <a name="_toc348891596"></a><a name="_toc349891494"></a>**Limitations**
1. The communication between agent and server relies on UDP port 1514 UDP to be open between two ends
1. UAC may be blocking the OSSEC service from communicating with the manager on Windows 

   1. ##### <a name="_toc349891495"></a>**Affected Area**
- All NADRA critical applications.
  1. ##### <a name="_toc348891597"></a><a name="_toc349891496"></a>**References** 
[1] <http://httpd.apache.org/docs/1.3/logs.html#accesslog>

[2] <http://httpd.apache.org/docs/current/mod/mod_log_config.html>
1. #### <a name="_toc348891598"></a><a name="_toc349891497"></a>**Reference ID: 1.3.3.4**
   1. ##### <a name="_toc348891599"></a><a name="_toc349891498"></a>**Goal**
The use case will allow the SOC team to monitor and raise an alarm if concurrent logins in VeriSys have increased to 100 in 1 minute.

RESEARCH RELATED!! (Guardium one user One IP can do this?  Or discuss with ahmer) 


![](Aspose.Words.74e725a8-9807-4d94-8b20-a5fea5e2882c.012.png)





1. #### <a name="_toc348891600"></a><a name="_toc349891499"></a>**Reference ID: 1.3.3.5**
   1. ##### <a name="_toc348891601"></a><a name="_toc349891500"></a>**Goal**
This use case allows the SOC team to detect if a sensitive application has been accessed from outside country.
1. ##### <a name="_toc348891602"></a><a name="_toc349891501"></a>**Sources**
Q1-radar SIEM console, CISCO firewall 
1. ##### <a name="_toc348891603"></a><a name="_toc349891502"></a>**Requirements**
Use Q1-radar appliance feature of GEOip lookup to identify traffic received to targeted applications coming from outside Pakistan.
1. ##### <a name="_toc348891604"></a><a name="_toc349891503"></a>**Audit to Event-ID mapping** 
N/A
1. ##### <a name="_toc348891605"></a><a name="_toc349891504"></a>**Troubleshooting**
For OSSEC use the troubleshooting steps given in section 4.1.1.1
1. ##### <a name="_toc348891606"></a><a name="_toc349891505"></a>**Dependency**
N/A
1. ##### <a name="_toc348891607"></a><a name="_toc349891506"></a>**Limitations**
N/A
1. ##### <a name="_toc349891507"></a>**Affected Area**
- All NADRA public facing critical applications.
  1. ##### <a name="_toc348891608"></a><a name="_toc349891508"></a>**References** 
N/A
1. #### <a name="_toc348891609"></a><a name="_toc349891509"></a>**Reference ID: 1.3.3.6**
   1. ##### <a name="_toc348891610"></a><a name="_toc349891510"></a>**Goal**
This use case will allow the SOC team to monitor if the server receives hits for sensitive resource (URI).
1. ##### <a name="_toc348891611"></a><a name="_toc349891511"></a>**Sources**
OSSEC (apache webserver, IIS)
1. ##### <a name="_toc348891612"></a><a name="_toc349891512"></a>**Requirements**
**Web-server**

`		`**Apache**

Monitor / alert when received GET to access sensitive URI

- RHEL / Red Hat / CentOS / Fedora Linux Apache access file location - **/var/log/httpd/access\_log**
- Debian / Ubuntu Linux Apache access log file location - **/var/log/apache2/access.log**
- FreeBSD Apache access log file location - **/var/log/httpd-access.log**

`		`**IIS**

Same applies in case of Apache.

- C:\Windows\System32\LogFiles\W3SVC1
  1. ##### <a name="_toc348891613"></a><a name="_toc349891513"></a>**Event to audit Mapping** 

|Details [1]||
| :- | :- |
|**Product:**|Apache|
|**Maps to**|4\.1.3.6|
|**Sensitive URI**||
|**Event Type**|Access log|
|**Source:**|W3SVC|
|**Description**|A process serving application pool 'DefaultAppPool' terminated unexpectedly. The process id was '1234'. The process exit code was '0xc0000005'.|











1. ##### <a name="_toc348891614"></a><a name="_toc349891514"></a>**Troubleshooting** 
For OSSEC use the troubleshooting steps given in section 4.1.1.1
1. ##### <a name="_toc348891615"></a><a name="_toc349891515"></a>**Dependency**
N/A
1. ##### <a name="_toc349891516"></a>**Affected Area**
- All NADRA critical applications.
  1. ##### <a name="_toc348891616"></a><a name="_toc349891517"></a>**Limitations**
N/A
1. ##### <a name="_toc348891617"></a><a name="_toc349891518"></a>**References** 
[1] http://www.ossec.net/
1. #### <a name="_toc348891618"></a><a name="_toc349891519"></a>**Reference ID: 1.3.3.7**
   1. ##### <a name="_toc348891619"></a><a name="_toc349891520"></a>**Goal**
This use case will allow the SOC team to monitor and detect if sip call is made from within NADRA to any foreign country other than authorized personnel’s.
1. ##### <a name="_toc348891620"></a><a name="_toc349891521"></a>**Sources**
Asterix 
1. ##### <a name="_toc348891621"></a><a name="_toc349891522"></a>**Requirements**
For asterix analyze the logs at following places /var/log/asterisk/messages or /var/log/asterisk/full for messages:-

- ‘international’ 

Examples:-

sip:joe.bloggs@212.123.1.213
sip:support@phonesystem.3cx.com
<sip:22444032@phonesystem.3cx.com>

**Enabling Syslog [1]**

/etc/asterisk/logger.conf:
























![](Aspose.Words.74e725a8-9807-4d94-8b20-a5fea5e2882c.013.png)








**For Fedora 10**

/etc/rsyslog.conf:
1. ##### <a name="_toc348891622"></a><a name="_toc349891523"></a>**Troubleshooting**
N/A
1. ##### <a name="_toc348891623"></a><a name="_toc349891524"></a>**Dependency**
List of the IP numbers those are authorized to dial international numbers
1. ##### <a name="_toc348891624"></a><a name="_toc349891525"></a>**Limitations**
Logs removed before sent to the Q1 for analysis.
1. ##### <a name="_toc349891526"></a>**Affected Area**
- All sip users.
  1. ##### <a name="_toc348891625"></a><a name="_toc349891527"></a>**References** 
[1] <http://kb.smartvox.co.uk/asterisk/secure-asterisk-pbx-part-2/>

[2] <http://blog.tmcnet.com/blog/tom-keating/asterisk/asterisk-hack-post-mortem.asp>

[3]http://wiki.shenhaoyu.com/doku.php?id=voip:asterisk:asterisk\_remote\_syslog
1. ### <a name="_toc348891626"></a><a name="_toc349891528"></a>**Sub-section ID: Policy violations** 
   1. #### <a name="_toc348891627"></a><a name="_toc349891529"></a>**Reference ID: 1.3.4.1** 
      1. ##### <a name="_toc348891628"></a><a name="_toc349891530"></a>**Goal**
Under this use-case the SOC operations team would be monitoring for credentials sent in clear text over network
1. ##### <a name="_toc348891629"></a><a name="_toc349891531"></a>**Sources**
`			`Ossec, (apache-webserver logs)
1. ##### <a name="_toc348891630"></a><a name="_toc349891532"></a>**Requirements**
**Method A**

`    `**Web-server** 

`            `Apache

`			`CustomLog logs/access.log "https://..." env=HTTPS

`			`CustomLog logs/access.log "http://..." env=!HTTPS

`			`SetEnv URL\_SCHEME=http

`			`SetEnvIf HTTPS on URL\_SCHEME=https

`			`CustomLog logs/access.log "%{URL\_SCHEME}e://..."

**Method B**

`			`**Apache**  

`			`**Parser the referrer header in http protocol as:-**

`			   `LogFormat "%{Referer}i %U" referrer

`			   `CustomLog /path/to/folder/referer.log referer

In Apache 2.x the LogFormat name referer appears to be reserved for the format "%{Referer}i -> %U". You should use a different name to prevent conflicts.

**IIS**

(Web Site Properties > Web Site Tab > Enable Logging > Properties)

![logging_properties.png](Aspose.Words.74e725a8-9807-4d94-8b20-a5fea5e2882c.014.png "logging_properties")










#####

1. ##### <a name="_toc348891631"></a><a name="_toc349891533"></a>**Troubleshooting**

For OSSEC use the troubleshooting steps given in section 4.1.1.1
1. ##### <a name="_toc348891632"></a><a name="_toc349891534"></a>**Limitations**
1. The communication between agent and server relies on UDP port 1514 UDP to be open between two ends

1. UAC may be blocking the OSSEC service from communicating with the manager on Windows 
   1. ##### <a name="_toc348891633"></a><a name="_toc349891535"></a>**Dependency**
N/A
1. ##### <a name="_toc349891536"></a>**Affected Area**
- All NADRA critical applications.
  1. ##### <a name="_toc348891634"></a><a name="_toc349891537"></a>**References** 
[1]http://serverfault.com/questions/359476/how-to-log-the-url-scheme-http-https-in-apache

[2] http://www.simonecarletti.com/blog/2009/01/logging-external-referers-with-apache/
1. #### <a name="_toc348891635"></a><a name="_toc349891538"></a>**Reference ID: 1.3.4.2**
   1. ##### <a name="_toc348891636"></a><a name="_toc349891539"></a>**Goal**
Under this use-case the SOC operations team would be monitoring and detecting any sensitive application is running on unpatched system.
1. ##### <a name="_toc348891637"></a><a name="_toc349891540"></a>**Sources**
Symantec End point, Nessus scan reports
1. ##### <a name="_toc348891638"></a><a name="_toc349891541"></a>**Requirements**
- Symantec End point

1. In the console, click Admin.
1. Click Servers.
1. Click the local site or remote site that you want to export log data from.
1. Click Configure External Logging.
1. On the General tab, select how often you want the log data to be sent to the file.
1. In the Master Logging Server list box, select the server you want to send logs to.

   If you use Microsoft SQL and have multiple management servers connected to the database, you only need one server to be the Master Logging Server.

1. Check Enable Transmission of Logs to a Syslog Server.
1. Configure the following fields as desired:

   - **Syslog Server**

Type in the IP address or domain name of the Syslog server that you want to receive the log data.

- **UDP Destination Port**

Type in the destination port that the Syslog server uses to listen for Syslog messages or use the default.


- **Log Facility**

Type in the number of the log facility that you want to be used in the Syslog configuration file or use the default. Valid values range from 0 to 23.

1. On the Log Filter tab, select all of the logs that you want to send to text files. If a log type that you select lets you select the severity level, check the severity levels that you want to save.

1. Click OK.
   1. ##### <a name="_toc348891639"></a><a name="_toc349891542"></a>**Audit to Event Id mapping** 
N/A
1. ##### <a name="_toc348891640"></a><a name="_toc349891543"></a>**Troubleshooting**
N/A
1. ##### <a name="_toc348891641"></a><a name="_toc349891544"></a>**Dependency** 
N/A
1. ##### <a name="_toc348891642"></a><a name="_toc349891545"></a>**Limitations**
N/A
1. ##### <a name="_toc349891546"></a>**Affected Area**
- All NADRA critical applications.

1. ##### <a name="_toc348891643"></a><a name="_toc349891547"></a>**References** 
[1]<http://www.symantec.com/business/support/index?page=content&id=HOWTO27571>
1. #### <a name="_toc348891644"></a><a name="_toc349891548"></a>**Reference ID: 1.3.4.2**
   1. ##### <a name="_toc348891645"></a><a name="_toc349891549"></a>**Goal**
Under this use-case the SOC operations team would be monitoring and detecting any configuration change in sensitive applications platforms
1. ##### <a name="_toc348891646"></a><a name="_toc349891550"></a>**Sources**
OSSEC
1. ##### <a name="_toc348891647"></a><a name="_toc349891551"></a>**Requirements**
Edit ossec.conf for following










![](Aspose.Words.74e725a8-9807-4d94-8b20-a5fea5e2882c.015.png)**File-system changes**





![](Aspose.Words.74e725a8-9807-4d94-8b20-a5fea5e2882c.016.png)**Registry**




**HIGH RISK REGISTRY ENTRIES LIST**

` `HKEY\_LOCAL\_MACHINE\System\CurrentControlSet\Services\\*

` `HKEY\_LOCAL\_MACHINE \SYSTEM\CurrentControlSet\Control\Session   Manager\\* particularly PendingFileRenameOperations

` `HKEY\_LOCAL\_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Image File Execution Options

` `HKEY\_LOCAL\_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run\\*

HKEY\_LOCAL\_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\RunOnce\\*

` `HKEY\_CURRENT\_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Run\\*

HKEY\_CURRENT\_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\RunOnce\\*





![](Aspose.Words.74e725a8-9807-4d94-8b20-a5fea5e2882c.017.png)**Network settings**



` `**Usb-settings**

|<p><agent\_config os="windows"></p><p>`  `<localfile></p><p>`    `<log\_format>full\_command</log\_format></p><p>`    `<command>reg QUERY HKLM\SYSTEM\CurrentControlSet\Enum\USBSTOR</command></p><p>`  `</localfile></p><p></agent\_config></p><p>***Configuration***</p>|
| :- |

Configure your Windows agents to monitor the USBSTOR registry









**Next create a local rule for that command:**

|<p><rule id="140125" level="7"></p><p>`    `<if\_sid>530</if\_sid></p><p>`    `<match>ossec: output: 'reg QUERY</match></p><p>`    `<check\_diff /></p><p>`    `<description>New USB device connected</description></p><p></rule></p><p>`  `***Configuration***</p>|
| :- |




1. ##### <a name="_toc348891648"></a><a name="_toc349891552"></a>**Audit to Event Id mapping** 
N/A
1. ##### <a name="_toc348891649"></a><a name="_toc349891553"></a>**Troubleshooting**
N/A
1. ##### <a name="_toc349891554"></a>**Affected Area**
- All NADRA critical applications.
  1. ##### <a name="_toc348891650"></a><a name="_toc349891555"></a>**Dependency** 
1. Make sure the agent is connected to the server. Agent connectivity can be verified by running the list\_agent utility at /var/ossec/bin/ directory with a –c switch.
1. Verify that there is no configuration error in the ossec.conf file and the syntax is correct. This can be verified by checking the ossec.log file in the agent machine.
   1. ##### <a name="_toc348891651"></a><a name="_toc349891556"></a>**Limitations**
N/A
1. ##### <a name="_toc348891652"></a><a name="_toc349891557"></a>**References** 
[1]  <a name="_hlt348867389"></a><a name="_hlt348867390"></a>[http://www.ossec.net/doc/manual/syscheck/index.html]()

[2]  <http://www.ossec.net/doc/syntax/head_ossec_config.global.html>

[3] <http://www.ossec.net/doc/syntax/head_ossec_config.client.html>

[4] http://www.ossec.net/doc/syntax/head\_ossec\_config.rootcheck.html
1. ### <a name="_toc348891653"></a><a name="_toc349891558"></a>**Sub-section ID: Legal**
   1. #### <a name="_toc348891654"></a><a name="_toc349891559"></a>**Reference ID: 1.3.5.1**
      1. ##### <a name="_toc348891655"></a><a name="_toc349891560"></a>**Goal**
Under this use-case the SOC operations team would be monitoring if high-profile individuals data has been accessed.
1. ##### <a name="_toc348891656"></a><a name="_toc349891561"></a>**Sources**
Ossec (running on Verisys web-server)
1. ##### <a name="_toc348891657"></a><a name="_toc349891562"></a>**Requirements**
**Web-server**

`	`**Apache**

Filter GET messages in log for following parameters:-

- nic

Fire an alarm if matching nic with high-profile personals. 
1. ##### <a name="_toc348891658"></a><a name="_toc349891563"></a>**Audit to Event Id mapping** 
N/A
1. ##### <a name="_toc348891659"></a><a name="_toc349891564"></a>**Troubleshooting**
N/A
1. ##### <a name="_toc348891660"></a><a name="_toc349891565"></a>**Limitations**
N/A
1. ##### <a name="_toc348891661"></a><a name="_toc349891566"></a>**Dependency**
N/A
1. ##### <a name="_toc349891567"></a>**Affected Area**
- All NADRA critical applications.
  1. ##### <a name="_toc348891662"></a><a name="_toc349891568"></a>**References** 
[1] http://www.ossec.net/
#####
|NADRA | ConfidentialUse-Case definition and Attributes|31|
| -: | :- |

