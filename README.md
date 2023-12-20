# CYS  

## Cross-Site Scripting (XSS) Vulnerability in Markdown Rendering 
### What is XSS? 
Cross-site scripting (also known as XSS) is a web security vulnerability that allows an attacker to 
compromise the interactions that users have with a vulnerable application. It allows an attacker to 
circumvent the same origin policy, which is designed to segregate different websites from each other. 
Cross-site scripting vulnerabilities normally allow an attacker to masquerade as a victim user, to carry 
out any actions that the user is able to perform, and to access any of the user's data. If the victim user 
has privileged access within the application, then the attacker might be able to gain full control over all 
of the application's functionality and data. 
# Technical Details 
1. **Severity** 
High
2. **Affected Components** 
The variety of attacks based on XSS is almost limitless, but they commonly include transmitting private 
data, like cookies or other session information, to the attacker, redirecting the victim to web content 
controlled by the attacker, or performing other malicious operations on the user's machine.
3. **Attack Vector** 
In reflected XSS, the attack vector is inside the HTTP client request processed by the server. If the 
server's request and response are semantically related, the server's response is formed from the request 
data. For example, the request could be a search query and the response might be the results page.
4. **Impact** 
cross site scripting attack can severely impact websites and web applications, damage their reputation 
and relationships with customers. XXS can deface websites, can result in compromised user accounts, 
and can run malicious code on web pages, which can lead to a compromise of the user's device.
# Exploitation of XSS 
Though, it is not a tough task to identify the XSS vulnerability, but most people don't know how to 
exploit it. As the exploitation techniques are tough and are not easily available on the web. Most people 
don’t know how they can take advantage of this vulnerability after they have successfully identified it in 
an application. 
1. **Step 1:** 
In our case, the parameter “VID” is vulnerable for Cross Site Scripting. After entering this payload in the 
URL, we got an alert box on the browser. This alert message confirms that the script was successfully 
executed, and the “VID” parameter of the form is vulnerable for XSS attacks.
2. **Step 2:** 
Now we can capture the user credentials by adding the malicious Java Script in the URL.
3. **Step 3:** 
We need to write the PHP code for ‘hehe.php’ through which the username and password will be 
dumped and saved on the attacker’s server. We can use free hosting servers for hosting this file. In our 
case we are using “000.webhost.com” server.
4. **Step 4:** 
Now, it’s time for action! Let us try to inject the URL with the java script that we have written. But, 
before putting the JavaScript into the URL, we need to encode it using a URL encoder. We can use 
http://meyerweb.com/eric/tools/dencoder/ website ( or any other online tool) for that.
# Tools for Exploitation
To discover and exploit an XSS vulnerability, an attacker must inject malicious code through client-side 
input parameters. The objective: to hijack the logic of a web application and allow, for example, the 
theft of cookies or session tokens, the alteration of data or content, the execution of malware, etc. 
1. OWASP ZAP 
OWASP ZAP is a free and open-source web application security scanner that can perform various types 
of XSS testing, such as reflected, stored, blind, and DOM-based. 
2. Burp Suite 
Burp Suite is a commercial web application security testing tool that can perform advanced XSS testing. 
3. XSStrike 
XSStrike is a free and open-source XSS detection and exploitation tool that can perform intelligent and 
dynamic XSS testing. 
4. Acunetix 
Acunetix is a commercial web application security scanner that can perform comprehensive XSS testing.
*All of these tools offer proxying, scanning, fuzzing, spidering, reporting, payload generation, filter 
evasion, crawler, encoder, and reverse shell features. They can be used as standalone tools or 
integrated with other tools or platforms.*
# Fixing the Vulnerability 
**Escaping user input** 
This is one way to prevent XSS vulnerabilities in applications. Escaping means taking the data an 
application has received and ensuring it's secure before rendering it for the user. Doing this prevents key 
characters in the data that a webpage receives from being interpreted as executable code. It prevents 
the browser from interpreting characters used to signal the start or end of executable code, and it 
translates them to escaped. 
**Sanitizing user input** 
Scrubs data clean of potentially executable characters. It changes unacceptable user input to an 
acceptable format and ensures the data received can't be interpreted as executable code. This approach 
is especially helpful on webpages that allow HTML markup. 
**Validating input** 
It makes certain an application is rendering the correct data and that malicious data does not harm a 
website, database and users. Validating input prevents XSS from being used in forms. It stops users from 
adding special characters into webpage data entry fields by refusing the request. 
**Mitigation** 
To mitigate the risk of XSS, it is crucial for web developers and application security teams to implement 
robust input validation and output encoding practices. Properly validating and sanitizing user input, as 
well as encoding output data to prevent script execution, are essential measures to protect against XSS 
attacks. 
# Conclusion 
In conclusion, Cross-Site Scripting (XSS) is a serious web application security vulnerability that allows 
attackers to inject malicious scripts into web pages viewed by other users. XSS can have significant 
consequences, including unauthorized access to user data, session hijacking, and the potential for 
spreading malware. The impact of XSS vulnerabilities can vary from minor nuisances to severe security 
breaches, depending on the context and the level of trust associated with the affected web application.
