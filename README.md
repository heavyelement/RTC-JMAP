# RTC-JMAP
Email is the lowest common denominator for online communication. Let's fix it.

# Goals
1. Based on the [JMAP protocol](https://jmap.io/), RTC-JMAP aims to provide open source Real Time Chat that is interoperable with legacy email 
2. Provide open source [email server](https://www.cyrusimap.org/index.html) software which facilitates Real Time Chat using JMAP protocols
  * This server software should provide IMAP functionality to allow backwards compatibility with legacy email protocols
  * Provide graceful fallback to older email protocols for email addresses that do not use JMAP
  * Legacy emails sent to RTC-JMAP accounts will be upgraded to JMAP inboxes
3. Provide website frontend, offer subscriptions for $5/month
  * Emails sent from the web frontend to legacy email accounts will have an invitation to join the Email 2.0 revolution
4. (Eventually) provide a client for mobile/desktops (perhaps RTC-JMAP plugins for existing clients?)

# Features
* Real Time/Near Real Time Chat
* Open source licensing of the spec/software
* Typing indicators
* Emoji reactions for individual emails
* Improved email chains
* Group chats
* Legacy email interoperability
* Standardized spam and phishing protection
