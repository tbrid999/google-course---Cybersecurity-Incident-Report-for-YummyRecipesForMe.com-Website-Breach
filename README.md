# google-course---Cybersecurity-Incident-Report-for-YummyRecipesForMe.com-Website-Breach

The investigation revealed the following network protocols were involved in the incident:

DNS (Domain Name System): Used to resolve the IP addresses of the URLs yummyrecipesforme.com and greatrecipesforme.com. The browser initiated DNS requests for these domains, and the DNS server provided their corresponding IP addresses.
HTTP (Hypertext Transfer Protocol): Used to request and deliver web pages and associated content. The HTTP protocol was used when the browser requested the yummyrecipesforme.com page and later redirected to greatrecipesforme.com.
TCP (Transmission Control Protocol): Underlying transport protocol used to establish connections between the browser and the web server.
Section 2: Summary of the Incident
The website yummyrecipesforme.com was compromised in a brute force attack executed by a former employee. The attacker exploited the use of a default password for the admin account to gain unauthorized access to the web host. After accessing the admin panel, the attacker made the following modifications:

Embedding Malware: The attacker injected JavaScript code into the website's source code. This code prompted visitors to download a malicious file under the pretext of updating their browser.
Redirecting Visitors: Upon executing the malicious file, users' browsers were redirected to a fake website, greatrecipesforme.com, which further spread malware.
Timeline of Events:

A brute force attack was launched, repeatedly attempting known default admin passwords.
The attacker gained admin access after guessing the correct password.
The attacker embedded malicious JavaScript in the website’s source code.
Customers reported suspicious activity, including prompts to download files and subsequent redirection to a different website.
The incident was confirmed when the hosting provider and cybersecurity team reviewed the source code and traffic logs.
Impact of the Incident:

For Customers: Malware was downloaded to customers' devices, causing performance issues and potential exposure of sensitive data.
For the Organization: The brand’s reputation suffered due to the compromise, and the website became a security risk to its users.
Sources of Evidence:

Traffic Logs: Captured using tcpdump, revealing DNS and HTTP activity between the browser and web servers.
Source Code Analysis: JavaScript code embedded to deliver malware was identified by senior analysts.
Section 3: Recommendation for Preventing Brute Force Attacks
Recommended Measure: Enforce Two-Factor Authentication (2FA)

Why 2FA is Effective: Two-factor authentication adds an additional layer of security to user accounts by requiring a second factor of authentication (e.g., a one-time password sent to a mobile device or email) in addition to the standard username and password. Even if a malicious actor successfully guesses or steals the password, they will be unable to access the account without the second authentication factor.

Benefits:

Increased Security: Prevents unauthorized access even if the password is compromised.
Resistance to Brute Force Attacks: Password guessing alone will not suffice, significantly reducing the effectiveness of brute force attacks.
Ease of Implementation: Many services provide built-in 2FA capabilities, making deployment straightforward.
By implementing 2FA and reviewing login policies, the organization can significantly reduce the risk of similar breaches in the future. Additionally, requiring strong passwords, monitoring login attempts, and limiting login retries should be integrated into the security framework to further enhance protection.

