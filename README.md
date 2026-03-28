# Investigating Failed Logon Attempts on Windows with Event Viewer

## Objective
Use Event Viewer to identify failed logon attempts on a Windows system by filtering the Security log for Event ID 4625 and reviewing event details relevant to authentication troubleshooting and basic security monitoring.

## Tools Used
- Windows Server 2019
- Event Viewer
- Windows Security Log

## Environment Used
- Windows Server 2019

## Lab Description
This lab focuses on identifying failed logon attempts in Windows using Event Viewer. Reviewing failed authentication events is an important part of system administration, troubleshooting, and basic security monitoring. In this exercise, I used the Windows Security log to filter for failed logon events and review the details associated with each attempt.

## Skills Demonstrated
- Navigating Windows Event Viewer
- Filtering Windows Security logs by Event ID
- Identifying failed authentication activity
- Reviewing event details for basic investigation
- Documenting technical findings in a structured format

## Procedure

---

From the taskbar, click the **Windows Start** icon, then open **Event Viewer**.

![Event Viewer](https://user-images.githubusercontent.com/107451613/176720521-8e7da4c8-44e9-4948-9167-c77f058f29c4.png)

---

From the left pane, navigate to **Event Viewer > Windows Logs > Security** to open the Security log in the center pane. The Security log contains authentication-related events, including successful and failed logon attempts.

![Security Log Navigation](https://user-images.githubusercontent.com/107451613/176721970-0d5992e5-020e-4f73-a3df-fbd49357162e.png)

---

On the far right, locate the **Actions** pane and click **Filter Current Log** to open the filter dialog box.

![Filter Current Log](https://user-images.githubusercontent.com/107451613/176723795-93bda28b-0072-4ba8-a225-dd397046aaf0.png)

---

In the **<All Event IDs>** field, type **4625** and click **OK** to apply the filter.

![Event ID 4625 Filter](https://user-images.githubusercontent.com/107451613/176724604-3d87da87-20a8-4147-b2c4-555f47765214.png)

---

After filtering, the center pane will display failed logon attempts. Repeated failed attempts against the same account or a high number of failures within a short period may require further investigation.

Double-click a failed logon event to open the **Event Properties** dialog box. This window provides additional details such as:
- date and time of the event
- failure reason
- target username
- source IP address
- source port
- process name associated with the event

## Investigation Notes
When reviewing Event ID 4625, I focused on the following fields:
- **Account Name**
- **Failure Reason**
- **Logon Type**
- **Source Network Address**
- **Source Port**
- **Time Created**

These details help provide context around failed authentication attempts and can support troubleshooting or further security investigation.

## Key Takeaways
- Event ID **4625** identifies failed logon attempts in Windows.
- Event Viewer provides useful security information for troubleshooting and monitoring.
- Repeated failed logon attempts may indicate password issues, user error, or suspicious activity.
- Reviewing event details such as usernames, timestamps, and source IP addresses can help support investigation.

## Why This Matters
Knowing how to identify failed logon attempts is a useful foundational skill in IT and cybersecurity. System administrators, help desk staff, and security analysts rely on event logs to investigate authentication issues, review suspicious activity, and better understand what is happening on a system.
