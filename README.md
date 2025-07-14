# Web Login Brute Force Script

## Objective  
Automate credential stuffing attacks against a web login form using Python, simulating how attackers test combinations of common usernames and passwords against exposed or weak web applications.

## Skills Learned

- **Credential Stuffing Logic**: Implemented nested brute-force logic combining multiple usernames with a common password list.
- **HTTP Request Crafting**: Used `requests.post()` to interact with a real login endpoint and check for successful logins.
- **Response Pattern Matching**: Detected successful logins by searching for a specific string (`"Welcome back"`) in HTTP response content.
- **Progress Logging**: Built real-time terminal output using `sys.stdout` to show which credentials were being tested.
- **File & String Handling**: Parsed text files securely and handled encoding for web form compatibility.

## Tools Used

- **Python 3**: Core language used for scripting the attack logic.
- **Requests**: Python HTTP library to submit POST login attempts.
- **Kali Linux CLI**: Environment for script execution and managing password files.

## Steps

1. Define the target URL and list of usernames.
2. Read the top-100 password list from a file.
3. Loop through each username.
4. For each username, try every password by sending a POST request to the login form.
5. Check if the response contains the success keyword (`"Welcome back"`).
6. Print valid username-password combinations when found.
7. Exit the script once a valid login is detected.

<img width="1539" height="692" alt="image" src="https://github.com/user-attachments/assets/5f557136-1666-49e6-b8cc-ae0717087383" />

Invalid credentials input:

<img width="552" height="233" alt="image" src="https://github.com/user-attachments/assets/fe65a2ac-881e-4f21-9531-df9e4917477f" />

Valid credentials input:

<img width="534" height="216" alt="image" src="https://github.com/user-attachments/assets/5197937d-c1fd-40c6-b9e1-288f3a58eeda" />

Script output on successful credentials match:

<img width="935" height="259" alt="image" src="https://github.com/user-attachments/assets/1a086dea-2efa-4e41-8d69-c37c13637e6b" />
