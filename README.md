# RTC-JMAP
Email is the lowest common denominator for online communication. Let's fix it.

# Goals
1. Based on the [JMAP protocol](https://jmap.io/), RTC-JMAP aims to provide open source Real Time Chat in the email  
2. Provide open source [email server](https://www.cyrusimap.org/index.html) software which facilitates Real Time Chat using JMAP email
  * This server software should provide IMAP functionality to allow backwards compatibility with legacy 
  * Provide graceful fallback to older email protocols for email addresses that do not use JMAP
  * Legacy emails sent to RTC-JMAP accounts will be delivered successfully to JMAP inboxes
3. Provide website frontend, offer subscriptions for $5/month
  * Emails sent from the web frontend to legacy email accounts will have an invitation to join the Email 2.0 revolution
4. (Eventually) provide a client for mobile/desktops (perhaps RTC-JMAP plugins for existing clients?)

# Features
* Real Time/Near Real Time Communication
* Typing indicators
* Emoji reactions for individual emails
* Improved email chains
* Group chats
* Standardized spam and phishing protection
* Legacy email interoperability
