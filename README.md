# Using-Wireshark---analyzing-web-browser-artifacts-email-header-analysis
## AIM:
To use Wireshark to analyze web browser activities and inspect email headers from captured network traffic.

## DESIGN STEPS:
### Step 1:
Launch Wireshark and start capturing traffic on the appropriate network interface.

### Step 2:
Use filters like http, dns, or tcp.port == 80 to monitor web browser artifacts such as visited URLs, cookies, and user-agent strings.

### Step 3:
Apply filters like smtp, pop, or imap to locate and analyze email header details (e.g., sender, receiver, subject) from email communications.

## PROGRAM:
Wireshark Web and Email Traffic Filtering Steps

## OUTPUT:
Captured Web Activity and Email Header Information A. Capturing Traffic in Wireshark

Open Wireshark and start capturing on the active interface (Wi- Fi/Ethernet).

Perform activities like opening a website or sending an email through a client (e.g., Gmail via browser or Thunderbird).

Stop the capture once done.
![image](https://github.com/user-attachments/assets/c3102d14-3c29-4ed0-82aa-d3dddf13c435)

Analyze DNS Queries: o Filter: dns

o Reveal domains the browser tried to resolve.
![image](https://github.com/user-attachments/assets/eed59de3-b660-4b91-a6b6-46ca9d445dbe)

mail Header Analysis

Apply relevant filters: o For POP3: tcp.port == 110

o For SMTP: tcp.port == 25 or 587

o For IMAP: tcp.port == 143 or 993

Locate email data: o Look for SMTP packets to see sender/receiver email addresses.

o Use "Follow TCP Stream" to view the full email headers and body if unencrypted.

Extract Email Header Fields:

o Analyze From, To, Subject, Date, Message-ID, and relay servers used in sending the email.
![image](https://github.com/user-attachments/assets/bfcdf173-0348-40ea-b0dc-a5df34a9c0d4)

![image](https://github.com/user-attachments/assets/89529ff0-ee75-4238-89ed-218856b0b2a5)

![image](https://github.com/user-attachments/assets/8f404279-9276-490c-a37b-57475c53ea45)

## RESULT:
Web browser artifacts and email headers were successfully analyzed using Wireshark.

