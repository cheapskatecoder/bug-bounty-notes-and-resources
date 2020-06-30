# Web application hackers handbook - 2 Notes

## Chapter - 1 

### Early days of the web

The early days of the web only had essential information in it. No styling, no "click to read more", just imagine an RFC standard page.

However now a days there are permission handling dynamic websites, cute little popups that ask you to buy their shitty course on whatever topic you find yourself reading about.

<em>Note - Every web application is built differently and will break differently so don't get upset the critical vulnerability you found on your college website using Nessus will work on Google or Facebook as well. </em>

These are the top vulnerabilities still found in most of the web applications

1. Broken Authentication
2. Broken access controls 
3. SQL Injections
4. XSS
5. Information leakage
6. CSRF
7. XXE (XML External Entity)
8. Misconfiguration
9. Insecure serilalization/deserialization
10. Insufficient logging and monitoring

### The core security problems

User input is untrustworthy, they can enter their email ID when you ask for it, even their credit card number but if you dare ask them to keep a username with emojis and holy shit will your system break.

1. Any client side implemented controls can be circumvented so kiss your JS goodbye that you wrote in 3 hours for signup form validation. FYI, this also includes headers and cookies and shit.
2. Users can jump between sequences and enter parameters willy nilly and to check whether the desired sequences of actions have been followed is the job of the developer.
3. Users use a lot of shit to access the applicaiton, can be phones tablets, samsung smart TV, and there can be platform specific bugs that can cause you trouble.

Here's an example of how exactly can a user fuck your shit up.
1. Change the values in hidden fields, such as a price for a product.
2. Modifying tokens to access another user's session.
3. Removing attributes that are required in order to break  your logic.
4. Instead of writing their credit card number, they enter a SQL query. Gotta hate these type of users thought.

