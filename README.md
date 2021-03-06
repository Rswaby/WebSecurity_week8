# Project 8 - Pentesting Live Targets

Time spent: 11 hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each version of the site has been given two of the six vulnerabilities. (In other words, all six of the exploits should be assignable to one of the sites.)

## Blue

Vulnerability #1: SQL Injection
                This vulerability is located on Blue. hackers can inject sql queries such as ' OR SLEEP(5)=0--' as shown below.
                Other sites did not have this vulerability.
                - [ ] GIF Walkthrough: ![Alt Text](sqli_blue.gif)

Vulnerability #2: Session Hijacking/Fixation
                Using the /public/hacktools/change_session_id.php we can change the session id such that you can bypass the login. as shown below
                - [ ] GIF Walkthrough: ![Alt Text](blue_cookie_hack.gif)


## Green

Vulnerability #1: Username Enumeration
                For this vulerability, the deveoper made a mistake by leaving the error message bold when the correct username is inputed and
                the normal when the username is unrecognized.
                - [ ] GIF Walkthrough: ![Alt Text](GreenuserEnum.gif)


Vulnerability #2: Cross-Site Scripting
                  1) leave a message for the admin in the "contact" with a xss.
                  2) login as the admin to the result.
                - [ ] GIF Walkthrough: ![Alt Text](green_xss.gif)


## Red

Vulnerability #1:  Insecure Direct Object Reference
                  This  vulerability was located in the Salesperson link, the url could be changed such that the Salesperson can be changed
                  the Salesperson and id=10 was not suppose to be reveal.
                  But on the other sites the developers made it such that if id=10 was inputed then it would redirect to all the Salespersons
                - [ ] GIF Walkthrough: ![Alt Text](Red_IOR_.gif)

Vulnerability #2: Cross-Site Request Forgery
                using the form in Cross-site_Request.html we open the file in a browser and change one of the existing user information
                - [ ] GIF Walkthrough: ![Alt Text](Cross-Site_Request.gif)

## Notes

Describe any challenges encountered while doing the work
