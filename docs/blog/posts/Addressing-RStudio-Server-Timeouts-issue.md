---
date:
  created: 2025-08-01
  #Sometimes, bloggers need to update a post. This might happen when you make a mistake or when something changes that you need to reflect in the post. To indicate you have edited a post, you can include an updated date in the page header.
  updated: 2025-08-05


categories:
  - Anvil

tags:
  - Rstudio
  - Open OnDemand
authors:
  - jin456

---

# Addressing RStudio Server Timeouts issue

RStudio Server times out after approximately 60 minutes of inactivity. Upon re-entering the session, users are often face login screen where their credentials do not work. (Example ticket: [TDX-510085](https://service.purdue.edu/TDNext/Apps/33/Tickets/TicketDet?TicketID=510085))

<!-- more -->

This issue is related to the RStudio Server configuration that sessions will automatically log out if inactive for over 60 minutes. The solution would be either to keep active every 60 minutes or use the user name and password (session specific password) described as follows to re-login:

1. Navigate to the current RStudio session in Open OnDemand.
2. Click on the session ID to open the session folder. (See attached picture).
![](https://github.rcac.purdue.edu/RCAC-Staff/SupportKnowledgeBase/blob/master/pics/OOD-R-timeout.png)

3. Locate the connection.yml file within the session folder. (See attached picture).
![](https://github.rcac.purdue.edu/RCAC-Staff/SupportKnowledgeBase/blob/master/pics/OOD-R-timeout-2.png)

4. Open it to find the session-specific password. (See attached picture).
![](https://github.rcac.purdue.edu/RCAC-Staff/SupportKnowledgeBase/blob/master/pics/OOD-R-timeout-3.png)
5. Then, use your Purdue account username in the "Username" field.

6. Enter the password retrieved from the connection.yml file.

P.S. If you could not open the page after re-login and saw the web url ended with '/appUri', delete '/appUri' and retry with the remaining url. 

These steps can be done by the user.