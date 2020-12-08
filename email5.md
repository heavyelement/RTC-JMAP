Email 5.0 (WIP)

Goals:

1. Clients/servers adopt a push-notification model
   1. Email 5.0 should be fast enough that real-time text chat is possible in optimal scenarios.
2. Setting up email clients should be as simple as providing
   1. Email address
   2. Password/TFA token
   3. Server domain (optional, MX record for email domain should intelligently handle this)
3. Distributed database (blockchain) of public keys/spam domains (?)
4. All sensitive data is end-2-end encrypted by default
5. Conversation UUID for email chains

Server:

1. JMAP is the basis for this protocol.
2. The server will function as a standard web host with certain predefined URIs which facilitate communication with other servers
   1. <domain>/capabilities - a list of the capabilities of a server in JSON format
      * Capabilities include read-reciepts, reaction emojis, end-to-end encryption, username tags (<name>+<tag>@<domain>)
   2. <domain>/version - protocol version
3. The server will send push notifications upon receipt of a new email

Client:


Email:
1. Email body, subject, UUID, attachments, etc are end-to-end encrypted
2. Emails have a single styling mode: markdown
   1. md engine should support tables
3. Email signatures are sent as a separate field in the email data rather than as part of the body
4. Emails from marketing companies like Mailchimp must have
5. Email replies only contain the body content of the message being sent and not a nested email chain
6. Email data contains:
```
   {
       "to": ["user@example.com"],
       "from": "gardiner@heavyelement.io",
       "sent": 1606936871434,
       "conversation_id": "aafa9a2f-310a-4a7e-963f-0e17ccdb398f",
       "message_id": "723e468a-32ca-437d-8352-81fe903b5e78",
       "subject": "Hello World",
       "content": "Hey there, just wanted to make sure you got this image! ![jump.png](jump.png) ",
       "attachments": [
           {
               "encoding": "text/base64",
               "content": <base64>,
               "filename": "jump.png"
           }
       ]
   }
```
