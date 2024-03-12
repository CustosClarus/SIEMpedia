# **SIEM USE CASEs configuration** 
## Baselining the systems against SOC operational requirements

## TABLE OF CONTENTS
1. Background	[here](#Background)
2. Scope	
3. Responsibility
 - 3.1. SOC team	
 - 3.2.	GRC Team	
 - 3.3.	Internal Audit	
3.4.	Systems / Control owners	
3.5.	Management	
5. Use-Case definition and Attributes	
4.1.	Section ID: Application	
4.1.1. Sub-section ID: Inside Attack	
4.1.1.1. Reference ID: 1.3.1.1.	
4.1.1.1.1. Goal	
4.1.1.1.2. Sources	
4.1.1.1.3. Requirements	
4.1.1.1.4. Troubleshooting steps	
4.1.1.1.5. Event to ID mapping	
4.1.1.1.6. Dependency	
4.1.1.1.7. Affected Area	
4.1.1.1.8. Limitations	
4.1.1.1.9. References	
4.1.1.2. Reference ID: 1.3.1.2	12
4.1.1.2.1. Goal	
4.1.1.2.2. Sources	
4.1.1.2.3. Requirements	
4.1.1.2.4. Event to ID mapping	
4.1.1.2.5. Troubleshooting steps	13
4.1.1.2.6. Dependency	13
4.1.1.2.7. Limitations	13
4.1.1.2.8. Affected area	13
4.1.1.2.9. References	13
4.1.2. Sub-section ID: External Attack	14
4.1.2.1. Reference ID: 1.3.2.1	14
4.1.2.1.1. Goal	14
4.1.2.1.2. Sources	14
4.1.2.1.3. Requirements	14
4.1.2.1.4. Event to ID mapping	14
4.1.2.1.5. Troubleshooting steps	14
4.1.2.1.6. Dependency	14
4.1.2.1.7. Limitations	15
4.1.2.1.8. Affected Area	15
4.1.2.1.9. References	15
4.1.3. Sub-section ID: Visibility	15
4.1.3.1. Reference ID: 1.3.3.1	15
4.1.3.1.1. Goal	15
4.1.3.1.2. Sources	15
4.1.3.1.3. Requirements	15
4.1.3.1.4. Audit to Event-ID mapping	16
4.1.3.1.5. Limitations	16
4.1.3.1.6. Troubleshooting steps	16
4.1.3.1.7. Dependency	16
4.1.3.1.8. Affected Area	16
4.1.3.1.9. References	16
4.1.3.2. Reference ID: 1.3.3.2	16
4.1.3.2.1. Goal	16
4.1.3.2.2. Sources	16
4.1.3.2.3. Requirements	16
4.1.3.2.4. Event to Audit ID Mapping	17
4.1.3.2.5. Troubleshooting	18
4.1.3.2.6. Dependency	18
4.1.3.2.7. Limitations	18
4.1.3.2.8. Affected Area	18
4.1.3.2.9. References	18
4.1.3.3. Reference ID: 1.3.3.3	18
4.1.3.3.1. Goal	18
4.1.3.3.2. Sources	18
4.1.3.3.3. Requirements	18
4.1.3.3.4. Troubleshooting	18
4.1.3.3.5. Auditing to Event-ID Mapping	19
4.1.3.3.6. Dependency	19
4.1.3.3.7. Limitations	19
4.1.3.3.8. Affected Area	19
4.1.3.3.9. References	19
4.1.3.4. Reference ID: 1.3.3.4	19
4.1.3.4.1. Goal	19
4.1.3.5. Reference ID: 1.3.3.5	19
4.1.3.5.1. Goal	19
4.1.3.5.2. Sources	19
4.1.3.5.3. Requirements	19
4.1.3.5.4. Audit to Event-ID mapping	20
4.1.3.5.5. Troubleshooting	20
4.1.3.5.6. Dependency	20
4.1.3.5.7. Limitations	20
4.1.3.5.8. Affected Area	20
4.1.3.5.9. References	20
4.1.3.6. Reference ID: 1.3.3.6	20
4.1.3.6.1. Goal	20
4.1.3.6.2. Sources	20
4.1.3.6.3. Requirements	20
4.1.3.6.4. Event to audit Mapping	21
4.1.3.6.5. Troubleshooting	21
4.1.3.6.6. Dependency	21
4.1.3.6.7. Affected Area	21
4.1.3.6.8. Limitations	21
4.1.3.6.9. References	21
4.1.3.7. Reference ID: 1.3.3.7	21
4.1.3.7.1. Goal	21
4.1.3.7.2. Sources	21
4.1.3.7.3. Requirements	21
4.1.3.7.4. Troubleshooting	22
4.1.3.7.5. Dependency	22
4.1.3.7.6. Limitations	22
4.1.3.7.7. Affected Area	22
4.1.3.7.8. References	22
4.1.4. Sub-section ID: Policy violations	22
4.1.4.1. Reference ID: 1.3.4.1	22
4.1.4.1.1. Goal	22
4.1.4.1.2. Sources	23
4.1.4.1.3. Requirements	23
4.1.4.1.4. Troubleshooting	24
4.1.4.1.5. Limitations	24
4.1.4.1.6. Dependency	24
4.1.4.1.7. Affected Area	24
4.1.4.1.8. References	24
4.1.4.2. Reference ID: 1.3.4.2	24
4.1.4.2.1. Goal	24
4.1.4.2.2. Sources	24
4.1.4.2.3. Requirements	24
4.1.4.2.4. Audit to Event Id mapping	25
4.1.4.2.5. Troubleshooting	25
4.1.4.2.6. Dependency	25
4.1.4.2.7. Limitations	25
4.1.4.2.8. Affected Area	25
4.1.4.2.9. References	26
4.1.4.3. Reference ID: 1.3.4.2	26
4.1.4.3.1. Goal	26
4.1.4.3.2. Sources	26
4.1.4.3.3. Requirements	26
4.1.4.3.4. Audit to Event Id mapping	27
4.1.4.3.5. Troubleshooting	27
4.1.4.3.6. Affected Area	27
4.1.4.3.7. Dependency	28
4.1.4.3.8. Limitations	28
4.1.4.3.9. References	28
4.1.5. Sub-section ID: Legal	28
4.1.5.1. Reference ID: 1.3.5.1	28
4.1.5.1.1. Goal	28
4.1.5.1.2. Sources	28
4.1.5.1.3. Requirements	28
4.1.5.1.4. Audit to Event Id mapping	28
4.1.5.1.5. Troubleshooting	28
4.1.5.1.6. Limitations	28
4.1.5.1.7. Dependency	29
4.1.5.1.8. Affected Area	29
4.1.5.1.9. References	29

Document Information

Document Title
Incident Response Policy
Drafted by
CustosClarus IS Operations team
Draft Date
Jan 5, 2013
Owner
CustosClarus
Classification/ Classification Authority
Internal / CustosClarus
Release Version
1.1
Reference document 
SOC implementation plan
Approval Date

Approved By

Published Date







### 1. Background
The purpose of this document is to illustrate assets owners the underlying procedural requirements and configurations necessary to operate and sustain SOC operations. The understanding of these requirements by owners is critically important in determining the success of SOC operations, In case of any change resulting due to improper configuration or management of these requirements can directly impact the performance of SOC operations team in timely detection and response to security incidents.
    2. Scope
The scope of this exercise stretches within the bounds of use-cases requirements mentioned in the SOC implementation plan referenced above (Document Information).
    3. Responsibility 
        3.1. SOC team 
The team is responsible for:-
    • Maintaining an auditable trail to prove events of interest were followed up on and resolved.
    • Active monitoring of controls

        3.2.  GRC Team
The team is responsible to update, maintain policies for relevancy and to reflect the configuration requirements herein mentioned.
        3.3.  Internal Audit 
The audit is responsible for:-
    • Reviewing the internal controls, periodically or as mentioned in annual audit plan or as directed by the regulator, implemented by senior management. 
    • Internal auditors will evaluate and review the internal controls in place and report for its improvements. 
    • To ensure that SOPs are followed by concerned department and grey areas, if any, are identified with recommendations how to counter the same.
        3.4.  Systems / Control owners 
The owners are responsible for:-
    • Introducing internal Controls through SOPs which are prepared in consultation with respective departmental heads, reviewed and approved by management for implementing the same.
    • Configuration and management of audit rules as per policies (e.g Change and configuration management policy).
        3.5.  Management
The management is responsible for:-
    • Establishing a mechanism to update the audit procedures.
    • Establishing a periodic review of audit activities and to adjust those audit activities to better support the CustosClarus’s business goals
    4. Use-Case definition and Attributes
        4.1. Section ID: Application
            4.1.1. Sub-section ID: Inside Attack
                4.1.1.1. Reference ID: 1.3.1.1.
                    4.1.1.1.1. Goal
Under this use-case the SOC operations team would be abnormal traffic pattern in non-business hours
                    4.1.1.1.2.  Sources
Web Server, HIDS, Q-Flow
                    4.1.1.1.3. Requirements
    1. Web Server [1]
    • Apache logs collection
Monitoring a log file
    1. Make changes in  /var/ossec/etc/ossec.conf

<ossec_config>
  <localfile>
    <log_format>apache</log_format>
    <location>/var/log/apache/access_log</location>
  </localfile>
</ossec_config
    2. IIS server [2]
    1. By default, the installation scripts will attempt to configure OSSEC to monitor the first virtual hosts for web (W3SVC1 to W3SVC254), ftp (MSFTPSVC1 to MSFTPSVC254) and smtp (SMTPSVC1 to SMTPSVC254)
   




























































<localfile>
    <location>%WinDir%\System32\LogFiles\W3SVC3\ex%y%m%d.log</location>
    <log_format>iis</log_format>
</localfile>





















                    4.1.1.1.4. Troubleshooting steps
    a. Enable debug mode


















If this is on an OSSEC server you can enable debug by running:



Enable debug mode and restart the OSSEC processes to view more verbose logs.

There is a firewall between the agent and the server.






    b. Wrong authentication keys configured (you imported a key from a different agent).


If that’s the case, you would be getting logs similar to the above on the agent and the following on the server (see also Errors:1403):




    c. Agent won’t connect to the manager or the agent always shows never connected














Step by Step – adding the authentication keys
For most of the errors (except the firewall issue), removing and re-adding the authentication keys fix the problem. Do the following if you are having issues:
    1. ‘Stop the server and the agent.’
        ◦ Make sure they are really stopped (ps on Unix or sc query ossecsvc on Windows)
    2. Run the manage-agents tool on the server and remove the agent.
    3. Still on the server, add the agent using manage-agents. Make sure the IP is correct.
    4. Start the server.
    5. Run manage-agents on the agent and import the newly generated key.
    6. Start the agent.
If after that, it still doesn’t work, contact our mailing list for help.
For additional information regarding troubleshooting refer to reference section
                    4.1.1.1.5. Event to ID mapping 
N/A
                    4.1.1.1.6. Dependency 
N/A
                    4.1.1.1.7. Affected Area
    • All CustosClarus domain machines.
    • Critical unix servers
    • Core network devices (public facing)

                    4.1.1.1.8. Limitations
    1. The communication between agent and server relies on UDP port 1514 UDP to be open between two ends

    2. UAC may be blocking the OSSEC service from communicating with the manager on Windows 
                    4.1.1.1.9. References 
[1] http://devio.us/~ddp/ossec/docs27/ossec101/managing_agents/localfile.html
[2] http://www.ossec.net/doc/manual/monitoring/file-log-monitoring.html
[3] http://www.ossec.net/doc/faq/unexpected.html
                4.1.1.2. Reference ID: 1.3.1.2
                    4.1.1.2.1. Goal
In this case SOC Operations Team would be detecting if buffer overflow event has taken place.
                    4.1.1.2.2. Sources
OSSEC, applications logs, firewall




                    4.1.1.2.3. Requirements 
        a. Ossec
Monitor for attack patter related to buffer-overflow (see below section for more details).





                    4.1.1.2.4. Event to ID mapping
Details [1]
Product:
OSSEC
Maps to
4.1.2.3.
Rule ID:
ID
Description 

40104
Possible buffer overflow attempt
Type
Buffer attack 

                    4.1.1.2.5. Troubleshooting steps
For OSSEC use the troubleshooting steps given in section 4.1.1.1
                    4.1.1.2.6. Dependency
Use this configuration 4.1.1.1 to setup apache and IIS.
                    4.1.1.2.7. Limitations
    1. The communication between agent and server relies on UDP port 1514 UDP to be open between two ends

    2. UAC may be blocking the OSSEC service from communicating with the manager on Windows 

                    4.1.1.2.8. Affected area
All critical applications
                    4.1.1.2.9. References 
http://www.ossec.net/doc/rules/rules/70_attack_rules.xml.html
            4.1.2. Sub-section ID: External Attack
                4.1.2.1. Reference ID: 1.3.2.1
                    4.1.2.1.1. Goal
In this case SOC Operations Team would be detecting for directory transversal attack.
                    4.1.2.1.2. Sources
OSSEC, applications logs, firewall
                    4.1.2.1.3. Requirements 
    a. Webserver 
            1. Apache & IIS
Monitor for attack patter related to directory transversal.









                    4.1.2.1.4. Event to ID mapping

Details [1]
Product:
OSSEC
Maps to
4.1.2.3.
Rule ID:
ID
Description 

31104
Possible directory transversal attempt
Type
Buffer attack 

                    4.1.2.1.5. Troubleshooting steps
For OSSEC use the troubleshooting steps given in section 4.1.1.1
                    4.1.2.1.6. Dependency
Use this configuration 4.1.1.1 to setup apache and IIS.
                    4.1.2.1.7. Limitations
    3. The communication between agent and server relies on UDP port 1514 UDP to be open between two ends

    4. UAC may be blocking the OSSEC service from communicating with the manager on Windows 

                    4.1.2.1.8. Affected Area
    • All CustosClarus critical applications
                    4.1.2.1.9. References 
http://www.ossec.net/doc/rules/rules/50_web_rules.xml.html

            4.1.3. Sub-section ID: Visibility 
                4.1.3.1. Reference ID: 1.3.3.1
                    4.1.3.1.1. Goal
Under this use-case the SOC operations team would be listing the number of applications user who have been authenticated to application and never to ADSources on a given day.
                    4.1.3.1.2. Sources
OSSEC, Active directory
                    4.1.3.1.3. Requirements
Enable apache to log username use this settings
    a. Apache
Start PHP as an Apache module (For PHP)
apache_note( 'username', $username );
In your server configuration make changes to file mod_log_config.c
LogFormat "%h %l %{username}n %t \"%r\" %>s %b" common_with_php_username
			          CustomLog logs/access_log common_with_php_username

Compare the recent application user login activity with AD user-session information, Fire alarm if a user has not logged in the day.

    b. Configure IIS to send attribute cs-username.[2]
			
                    4.1.3.1.4. Audit to Event-ID mapping 
N/A
                    4.1.3.1.5. Limitations
    1. The communication between agent and server relies on UDP port 1514 UDP to be open between two ends
    2. UAC may be blocking the OSSEC service from communicating with the manager on Windows 
                    4.1.3.1.6. Troubleshooting steps
For OSSEC use the troubleshooting steps given in section 4.1.1.1
                    4.1.3.1.7. Dependency 
N/A 
                    4.1.3.1.8. Affected Area
    • All CustosClarus critical applications.
                    4.1.3.1.9. References 
[1] http://stackoverflow.com/questions/3389169/put-username-in-apache-access-log-with-php-and-without-http-auth
[2]http://www.microsoft.com/technet/prodtechnol/WindowsServer2003/Library/IIS/676400bc-8969-4aa7-851a-9319490a9bbb.mspx?mfr=true
[2] http://httpd.apache.org/docs/2.2/mod/mod_log_config.html#customlog
                4.1.3.2. Reference ID: 1.3.3.2
                    4.1.3.2.1. Goal
The use case will allow the SOC team to monitor if the number of times a particular application has crashed on a given day.
                    4.1.3.2.2. Sources
OSSEC
                    4.1.3.2.3. Requirements
    a. Webserver
Apache view / get error.log for following messages 
            ▪ Apache service started
            ▪ SIGTERM, shutting down
RHEL / Red Hat / CentOS / Fedora Linux Apache error file location:-  /var/log/httpd/error_log
Debian / Ubuntu Linux Apache error log file location - /var/log/apache2/error.log
FreeBSD Apache error log file location –
/var/log/httpd-error.log

IIS view / get error in Application log related to following messages:-
            ▪ Faulting application w3wp.exe

       To locate IIS logs goto directory 
C:\Windows\System32\LogFiles\W3SVC1
                    4.1.3.2.4. Event to Audit ID Mapping 






















                    4.1.3.2.5. Troubleshooting
Use IIS State or DebugDiag tools[1]
                    4.1.3.2.6. Dependency
N/A
                    4.1.3.2.7. Limitations
N/A

                    4.1.3.2.8. Affected Area
    • All CustosClarus critical applications.
                    4.1.3.2.9. References 
[1] http://www.microsoft.com/en-us/download/details.aspx?id=26798
                4.1.3.3. Reference ID: 1.3.3.3
                    4.1.3.3.1. Goal
This use case allows the SOC team to detect if the user tries to upload suspicious .php file to the web-server.
                    4.1.3.3.2.  Sources
Ossec
                    4.1.3.3.3. Requirements
Webserver
        a. Apache
Use apache logs to analyze PUT / POST commands with identified extensions
Change / Append the log common format with attribute (%X)[2]
				       LogFormat "%h %X %l %u %t \"%r\" %>s %b" common

        b. IIS	
Same applies as above.
                    4.1.3.3.4. Troubleshooting
For OSSEC use the troubleshooting steps given in section 4.1.1.1
                    4.1.3.3.5. Auditing to Event-ID Mapping
N/A
                    4.1.3.3.6. Dependency
N/A
                    4.1.3.3.7. Limitations
    1. The communication between agent and server relies on UDP port 1514 UDP to be open between two ends
    2. UAC may be blocking the OSSEC service from communicating with the manager on Windows 

                    4.1.3.3.8. Affected Area
    • All CustosClarus critical applications.
                    4.1.3.3.9. References 
[1] http://httpd.apache.org/docs/1.3/logs.html#accesslog
[2] http://httpd.apache.org/docs/current/mod/mod_log_config.html
                4.1.3.4. Reference ID: 1.3.3.4
                    4.1.3.4.1. Goal
The use case will allow the SOC team to monitor and raise an alarm if concurrent logins in VeriSys have increased to 100 in 1 minute.






                4.1.3.5. Reference ID: 1.3.3.5
                    4.1.3.5.1. Goal
This use case allows the SOC team to detect if a sensitive application has been accessed from outside country.
                    4.1.3.5.2. Sources
Q1-radar SIEM console, CISCO firewall 
                    4.1.3.5.3. Requirements
Use Q1-radar appliance feature of GEOip lookup to identify traffic received to targeted applications coming from outside Pakistan.
                    4.1.3.5.4. Audit to Event-ID mapping 
N/A
                    4.1.3.5.5. Troubleshooting
For OSSEC use the troubleshooting steps given in section 4.1.1.1
                    4.1.3.5.6. Dependency
N/A
                    4.1.3.5.7. Limitations
N/A
                    4.1.3.5.8. Affected Area
    • All CustosClarus public facing critical applications.
                    4.1.3.5.9. References 
N/A
                4.1.3.6. Reference ID: 1.3.3.6
                    4.1.3.6.1. Goal
This use case will allow the SOC team to monitor if the server receives hits for sensitive resource (URI).
                    4.1.3.6.2. Sources
OSSEC (apache webserver, IIS)
                    4.1.3.6.3. Requirements
Web-server
		Apache
Monitor / alert when received GET to access sensitive URI
    • RHEL / Red Hat / CentOS / Fedora Linux Apache access file location - /var/log/httpd/access_log
    • Debian / Ubuntu Linux Apache access log file location - /var/log/apache2/access.log
    • FreeBSD Apache access log file location - /var/log/httpd-access.log
		IIS
Same applies in case of Apache.
        ◦ C:\Windows\System32\LogFiles\W3SVC1
                    4.1.3.6.4. Event to audit Mapping 











                    4.1.3.6.5. Troubleshooting 
For OSSEC use the troubleshooting steps given in section 4.1.1.1
                    4.1.3.6.6. Dependency
N/A
                    4.1.3.6.7. Affected Area
    • All CustosClarus critical applications.
                    4.1.3.6.8. Limitations
N/A
                    4.1.3.6.9. References 
[1] http://www.ossec.net/
                4.1.3.7. Reference ID: 1.3.3.7
                    4.1.3.7.1. Goal
This use case will allow the SOC team to monitor and detect if sip call is made from within CustosClarus to any foreign country other than authorized personnel’s.
                    4.1.3.7.2. Sources
Asterix 
                    4.1.3.7.3. Requirements
For asterix analyze the logs at following places /var/log/asterisk/messages or /var/log/asterisk/full for messages:-
            ▪ ‘international’ 

Examples:-
sip:joe.bloggs@212.123.1.213
sip:support@phonesystem.3cx.com
sip:22444032@phonesystem.3cx.com

Enabling Syslog [1]
/etc/asterisk/logger.conf:









For Fedora 10
/etc/rsyslog.conf:
                    4.1.3.7.4. Troubleshooting
N/A
                    4.1.3.7.5. Dependency
List of the IP numbers those are authorized to dial international numbers
                    4.1.3.7.6. Limitations
Logs removed before sent to the Q1 for analysis.
                    4.1.3.7.7. Affected Area
    • All sip users.
                    4.1.3.7.8. References 
[1] http://kb.smartvox.co.uk/asterisk/secure-asterisk-pbx-part-2/
[2] http://blog.tmcnet.com/blog/tom-keating/asterisk/asterisk-hack-post-mortem.asp
[3]http://wiki.shenhaoyu.com/doku.php?id=voip:asterisk:asterisk_remote_syslog
            4.1.4. Sub-section ID: Policy violations 
                4.1.4.1. Reference ID: 1.3.4.1 
                    4.1.4.1.1. Goal
Under this use-case the SOC operations team would be monitoring for credentials sent in clear text over network
                    4.1.4.1.2. Sources
			Ossec, (apache-webserver logs)
                    4.1.4.1.3. Requirements
Method A
    Web-server 
            Apache
			CustomLog logs/access.log "https://..." env=HTTPS
			CustomLog logs/access.log "http://..." env=!HTTPS

			SetEnv URL_SCHEME=http
			SetEnvIf HTTPS on URL_SCHEME=https
			CustomLog logs/access.log "%{URL_SCHEME}e://..."

Method B
			Apache  
			Parser the referrer header in http protocol as:-
			   LogFormat "%{Referer}i %U" referrer
			   CustomLog /path/to/folder/referer.log referer
In Apache 2.x the LogFormat name referer appears to be reserved for the format "%{Referer}i -> %U". You should use a different name to prevent conflicts.

IIS
(Web Site Properties > Web Site Tab > Enable Logging > Properties)













                    4.1.4.1.4. Troubleshooting

For OSSEC use the troubleshooting steps given in section 4.1.1.1
                    4.1.4.1.5. Limitations
    1. The communication between agent and server relies on UDP port 1514 UDP to be open between two ends

    2. UAC may be blocking the OSSEC service from communicating with the manager on Windows 
                    4.1.4.1.6. Dependency
N/A
                    4.1.4.1.7. Affected Area
    • All CustosClarus critical applications.
                    4.1.4.1.8. References 
[1]http://serverfault.com/questions/359476/how-to-log-the-url-scheme-http-https-in-apache
[2] http://www.simonecarletti.com/blog/2009/01/logging-external-referers-with-apache/
                4.1.4.2. Reference ID: 1.3.4.2
                    4.1.4.2.1. Goal
Under this use-case the SOC operations team would be monitoring and detecting any sensitive application is running on unpatched system.
                    4.1.4.2.2. Sources
Symantec End point, Nessus scan reports
                    4.1.4.2.3. Requirements
    • Symantec End point

    1. In the console, click Admin.
    2. Click Servers.
    3. Click the local site or remote site that you want to export log data from.
    4. Click Configure External Logging.
    5. On the General tab, select how often you want the log data to be sent to the file.
    6. In the Master Logging Server list box, select the server you want to send logs to.
If you use Microsoft SQL and have multiple management servers connected to the database, you only need one server to be the Master Logging Server.
    7. Check Enable Transmission of Logs to a Syslog Server.
    8. Configure the following fields as desired:

            ▪ Syslog Server
Type in the IP address or domain name of the Syslog server that you want to receive the log data.

            ▪ UDP Destination Port
Type in the destination port that the Syslog server uses to listen for Syslog messages or use the default.


            ▪ Log Facility
Type in the number of the log facility that you want to be used in the Syslog configuration file or use the default. Valid values range from 0 to 23.

    9. On the Log Filter tab, select all of the logs that you want to send to text files. If a log type that you select lets you select the severity level, check the severity levels that you want to save.

    10. Click OK.
                    4.1.4.2.4. Audit to Event Id mapping 
N/A
                    4.1.4.2.5. Troubleshooting
N/A
                    4.1.4.2.6. Dependency 
N/A
                    4.1.4.2.7. Limitations
N/A
                    4.1.4.2.8. Affected Area
    • All CustosClarus critical applications.

                    4.1.4.2.9. References 
[1]http://www.symantec.com/business/support/index?page=content&id=HOWTO27571
                4.1.4.3. Reference ID: 1.3.4.2
                    4.1.4.3.1. Goal
Under this use-case the SOC operations team would be monitoring and detecting any configuration change in sensitive applications platforms
                    4.1.4.3.2. Sources
OSSEC
                    4.1.4.3.3. Requirements
Edit ossec.conf for following
File-system changes




Registry
 


HIGH RISK REGISTRY ENTRIES LIST
 HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\*
 HKEY_LOCAL_MACHINE \SYSTEM\CurrentControlSet\Control\Session   Manager\* particularly PendingFileRenameOperations
 HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Image File Execution Options
 HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run\*
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\RunOnce\*
 HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Run\*
HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\RunOnce\*
Network settings



 Usb-settings
Configure your Windows agents to monitor the USBSTOR registry









Next create a local rule for that command:




                    4.1.4.3.4. Audit to Event Id mapping 
N/A
                    4.1.4.3.5. Troubleshooting
N/A
                    4.1.4.3.6. Affected Area
    • All CustosClarus critical applications.
                    4.1.4.3.7. Dependency 
    1. Make sure the agent is connected to the server. Agent connectivity can be verified by running the list_agent utility at /var/ossec/bin/ directory with a –c switch.
    2. Verify that there is no configuration error in the ossec.conf file and the syntax is correct. This can be verified by checking the ossec.log file in the agent machine.
                    4.1.4.3.8. Limitations
N/A
                    4.1.4.3.9. References 
[1]  http://www.ossec.net/doc/manual/syscheck/index.html
[2]  http://www.ossec.net/doc/syntax/head_ossec_config.global.html
[3] http://www.ossec.net/doc/syntax/head_ossec_config.client.html
[4] http://www.ossec.net/doc/syntax/head_ossec_config.rootcheck.html
            4.1.5. Sub-section ID: Legal
                4.1.5.1. Reference ID: 1.3.5.1
                    4.1.5.1.1. Goal
Under this use-case the SOC operations team would be monitoring if high-profile individuals data has been accessed.
                    4.1.5.1.2. Sources
Ossec (running on Verisys web-server)
                    4.1.5.1.3. Requirements
Web-server
	Apache
Filter GET messages in log for following parameters:-
            ▪ nic
Fire an alarm if matching nic with high-profile personals. 
                    4.1.5.1.4. Audit to Event Id mapping 
N/A
                    4.1.5.1.5. Troubleshooting
N/A
                    4.1.5.1.6. Limitations
N/A
                    4.1.5.1.7. Dependency
N/A
                    4.1.5.1.8. Affected Area
    • All CustosClarus critical applications.
                    4.1.5.1.9. References 
[1] http://www.ossec.net/
