# CTF-Challenge-on-Don-t-Bump-Your-Header


![image](https://github.com/user-attachments/assets/6ad16939-1d54-414c-853a-62c6ca72a93f)


## Objective

Try to bypass security measure on this site! http://165.227.106.113/header.php

### Skills Learned


## 🧠 Skills Learned

- 🔹 **HTTP Protocol Fundamentals** – Gained hands-on experience with request/response headers and status codes.
- 🔹 **User-Agent Spoofing** – Learned how to manipulate `User-Agent` strings to bypass security filters and access restricted content.
- 🔹 **Burp Suite Usage** – Intercepted and modified HTTP requests to analyze how servers handle different headers.
- 🔹 **Web Application Behavior Analysis** – Observed how applications respond to various header configurations.
- 🔹 **Bypassing Access Controls** – Practiced techniques used in real-world CTFs to evade user-agent-based restrictions.
- 🔹 **Manual Web Testing** – Enhanced skills in testing and crafting raw HTTP requests using tools like cURL, Postman, and browser dev tools.


### Tools Used
## 🛠️ Tools Used

- 🧰 **Burp Suite** – Intercepted, inspected, and modified HTTP requests and headers in real-time.
- 🌐 **Browser DevTools (Chrome)** – Used to monitor and edit HTTP headers directly within the browser.
- 🌀 **CURL** – Sent customized HTTP requests from the command line with modified headers.
- 📫 **Postman** – Crafted and tested HTTP requests with specific user-agent and header configurations.


## Steps
Step-by-Step Process On how I achieved this
-	Access the Challenge: I visited the provided URL http://165.227.106.113/header.php.
-	Initial Observation: I noticed that the website requires a specific user agent to access the content. I saw a comment in the HTML code: <!-- Sup3rS3cr3tAg3nt -->.
- Intercept Traffic: I used a tool like Burp Suite to intercept the HTTP request. Set Burp Suite to intercept mode by going to Proxy -> Intercept -> Intercept is on.

  ![image](https://github.com/user-attachments/assets/59f7682c-beda-4654-95f0-a4fee642fa26)

-	Modify User Agent: Changed the user agent in Burp Suite to Sup3rS3cr3tAg3nt. Forward the request and observe the response2.
-	Additional Security Measure: The website now requires that I appear as if I am coming from awesomesauce.com. This involves modifying the HTTP headers2.
-	Modify HTTP Headers: I added the Referer header to my request with the value awesomesauce.com. Turn off and on the intercept mode in Burp Suite, then refresh the page.
-	Exploitation: I used Curl to gain further access or retrieve hidden information. I found and captured the flag by navigating to the appropriate part of the application.
  
  ![image](https://github.com/user-attachments/assets/5f1339f0-be30-44ad-9a3b-2b8fa4884ace)

-	Obtain the Flag: After forwarding the modified request, I received the flag: flag{did_this_m3ss_with_y0ur_h34d}.

![image](https://github.com/user-attachments/assets/3176da0b-9e25-4f05-833e-dfe87b5832b4)

