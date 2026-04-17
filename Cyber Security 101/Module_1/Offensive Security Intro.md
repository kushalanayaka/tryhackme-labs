## Task 1: Think Like a Hacker

- Think like a attackers, Finding the vulnerabilities in the application before the real attackers.
- In this task, I have learned that offesive security requires a midset shift. Instead of using application as intended, attackers try to break logic,
exploit weakness, and discover hidden functionalities.

### Key Takeaways:
- Hackers explore beyond normal usage
- Focus on idetifing attack surfaces
- Enumeration is the first step in hacking.

### Screenshot
<img width="1328" height="489" alt="01_task1" src="https://github.com/user-attachments/assets/b0db1f3a-a42b-4121-bb77-85e543cc8083" />

<br>
<br>

## Task 2: Starting the Lab

- This task introduced the lab environment where I interact with a target system.
lab simulates real world application in a safe environment

- My task is to find the account number in the vulenarable fake bank site.
### Key Takeaways:
- Labs provides hands on experience
- Safe environment for practicing attackes
- Accessable via browser

### Screenshot
<img width="1360" height="606" alt="01_task2" src="https://github.com/user-attachments/assets/69891b7d-62af-47de-bc01-0db272039d1d" />

<br>
<br>

## Task 3: Find Hidden Pages

- In this task, I learned how attackers discover hidden web apges that are not diectly accessble
through the UI.
- I used `dirb http://fakebank.thm` command to find hidden url in the fakebank application
  and found `http://fakebank.thm/bank-transfer` hidden url.

### Techniques:
- Manual URL guessing (/bank-transfer, /images)
- Directory brute-forcing using tools like Dirb, Gobuster and ffuf

### Key Takeaways:
- Hidden pages can expose sensitive functionality
- Enumeration is critical in web security

### Screenshort
<img width="1363" height="633" alt="01_task3," src="https://github.com/user-attachments/assets/f59774fd-0fcd-46ea-8fb1-ac8071275f3a" />

<br>
<br>

## Task 4: Attack the Admin Page

- After discovering the admin page, the next step is to attempt to gain access.
- By adding `bank-transfer` to URL then selected account number `8881` and depoite `$2000`,
- to get `BANK-HACKED` massage to to complete the lab.

### Possible attack methods:
- Trying default credentials (admin:admin)
- Brute force attacks
- SQL Injection

### Key Takeaways:
- Admin panels are high-value targets
- Weak authentication mechanisms can be exploited

### Screenshort
<img width="1356" height="604" alt="01_task4" src="https://github.com/user-attachments/assets/42724b27-0704-476a-82c1-5ac11c574ba1" />

