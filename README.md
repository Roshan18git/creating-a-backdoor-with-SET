# creating-a-backdoor-with-SET
creating a backdoor with SET - Ethical Hacking Techniques course

# AIM:
To Create a backdoor with Social Engineering Toolkit (SET)

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode


### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

### Architecture Diagram

```
+----------------+        +------------------------+        +----------------------+
| Attacker's PC  | -----> | SET (Credential        | -----> | Fake Login Page      |
| (Kali Linux)   |        | Harvester via Apache)  |        | (Hosted by SET)      |
+----------------+        +------------------------+        +----------------------+
       |                                                             |
       |                                                             v
       |   1. Configure SET with phishing site (e.g., Gmail clone)   |
       |                                                             |
       |                                                             v
       |                                                 +----------------------+
       |                                                 | Victim's Browser     |
       | <------------------------------------------------| Clicks Phishing Link|
       |                                                 +----------------------+
       |                                                             |
       |                                                             v
       |     2. Victim Enters Credentials → Sent to SET/Attacker    |
       |                                                             |
       |                                                             v
       |                                                 +----------------------+
       |                                                 | Credentials Captured |
       |                                                 | in Apache log/SET DB |
       |                                                 +----------------------+

```

## EXECUTION STEPS AND ITS OUTPUT:
Social Engineering attacks are the various cons used by the hackers to trick people into providing sensitive data to the attackers.

**Steps to Use SET for Phishing (Credential Harvester Attack Method)**

**1. Open terminal:**
```bash
sudo setoolkit
```
<img width="1600" height="780" alt="image" src="https://github.com/user-attachments/assets/1c11a1a9-34bb-4760-9bb4-a99f60f85370" />

**2. Navigate:**
```bash
1) Social-Engineering Attacks  
2) Website Attack Vectors  
3) Credential Harvester Attack Method  
```
<img width="710" height="717" alt="image" src="https://github.com/user-attachments/assets/ab3543e5-d407-43de-aad5-1fa71b51065e" />

**3. Choose:**
```bash
2) Site Cloner
```
<img width="858" height="475" alt="image" src="https://github.com/user-attachments/assets/ccc57c59-3c08-4eaa-a059-f3fd884b12c3" />

**4. Enter the URL of the legitimate site ```(e.g., https://accounts.google.com)```**
<img width="745" height="216" alt="image" src="https://github.com/user-attachments/assets/b682eb02-567a-4ad0-abdc-f80f9a1bfa33" />

**5. Send the generated link to the victim.**
<img width="1504" height="663" alt="image" src="https://github.com/user-attachments/assets/d81a6cc8-e111-4852-a5a0-41e9c7eaeab7" />

**6. Once the victim logs in → their credentials are stored in:**
```bash
/var/www/html/
```
<img width="1057" height="396" alt="image" src="https://github.com/user-attachments/assets/9a776264-79f8-40f5-9566-cd25107904bd" />


## RESULT:
The Social Engineering Toolkit (SET) is used to create backdoor is  examined successfully
