# SOC-Automation

## Objective

This SOC Automation project aimed to establish a controlled environment for simulating and detecting cyber attacks. The primary focus was to ingest and analyze logs within a Security Information and Event Management (SIEM) system, generating test telemetry to mimic real-world attack scenarios. This hands-on experience was designed to deepen my understanding of network security, attack patterns, and defensive strategies.

### Skills Learned

- Advanced understanding of SIEM/SOAR concepts and practical application.
- Proficiency in analyzing and interpreting network logs.
- Ability to generate and recognize attack signatures and patterns.
- Enhanced knowledge of network protocols and security vulnerabilities.
- Development of critical thinking and problem-solving skills in cybersecurity.

### Tools Used

- Wazuh was the primary SIEM system used for log ingestion and analysis.
- Shuffle was utilized as my SOAR system used for automation and workflow management.
- Telemetry generation tools to create realistic network traffic and attack scenarios.

## Showcase

*Ref 1: Network Diagram*
![SOC Automation Project](https://github.com/joelkoszorus/SOC-Automation/assets/160312879/e8aae391-71fb-4e4d-b244-6d9c339f75bb)

*Ref 2: Wazuh Agent configured and active on Win10 VM*
![1](https://github.com/joelkoszorus/SOC-Automation/assets/160312879/9339bea1-e08f-46be-9edf-0ec9b1a7a1c7)

*Ref 3: Custom Wazuh rule was configure for detecting Mimikatz*
![2](https://github.com/joelkoszorus/SOC-Automation/assets/160312879/7a345e8f-5f9e-4d62-b4a3-9259953d17d3)

*Ref 4: For the detection demonstration the mimikatz filename is changed*
![3](https://github.com/joelkoszorus/SOC-Automation/assets/160312879/85e366f4-73a5-4328-87db-08c4818d47ae)
![4](https://github.com/joelkoszorus/SOC-Automation/assets/160312879/70933440-1ee1-4e5b-96ed-459466f161be)

*Ref 5: Mimikatz is then launched from powershell under it's altered filename on the Win10 VM. As configured, Wazuh successfully detects the malicious program after the filename has been changed, it does this by scanning for the .eventdata.originalFileName*
![5](https://github.com/joelkoszorus/SOC-Automation/assets/160312879/1328ce75-b43f-4dd7-a920-42be92251cd6)
![6](https://github.com/joelkoszorus/SOC-Automation/assets/160312879/69f96463-13ca-4153-a970-db850cac891d)

*Ref 6: Wazuh config file editted to integrate Shuffle*
![7](https://github.com/joelkoszorus/SOC-Automation/assets/160312879/681d95d5-6c84-4b46-9a60-95c671181fc4)

*Ref 7: After successful configuration an alert is sent to shuffle from Wazuh*
![8](https://github.com/joelkoszorus/SOC-Automation/assets/160312879/51500d67-da66-466c-85c1-a2303e48a4a4)

*Ref 8: Using Regex, Shuffle parses out the SHA256 hash value of the file which will be sent to VirsusTotal to check it's reputation score*
![9](https://github.com/joelkoszorus/SOC-Automation/assets/160312879/177e5614-cf26-4ab4-b018-b62ba8bf255a)
![10](https://github.com/joelkoszorus/SOC-Automation/assets/160312879/1bf77169-4f96-4384-afbd-f7d0cf32ccf0)

*Ref 9: TheHive is successfully configured in the Shuffle instance and an alert is created. The successful alert then populates TheHive client though Shuffle*
![11](https://github.com/joelkoszorus/SOC-Automation/assets/160312879/cd825212-db85-4d5a-811d-649cf7f25902)
![12](https://github.com/joelkoszorus/SOC-Automation/assets/160312879/e04486ac-d8aa-4134-b35f-4f261c1fe73b)

*Ref 10: An emailer is configured in Shuffle as well as an automated response feature for the SOC Analyst in this project environment*
![13](https://github.com/joelkoszorus/SOC-Automation/assets/160312879/35cb0229-2267-4b59-a230-8cba664766e3)

*Ref 11: The completed Shuffle SOAR workflow overview*
![14](https://github.com/joelkoszorus/SOC-Automation/assets/160312879/06fb3265-42db-4caf-b4c9-b0ef6caba22f)

