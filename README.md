# EG-SMTPd-Plugin
An Event Ghost plugin that uses SMTPd module to act as a basic SMTP server to trigger events in EG. 

Currently this plugin will simply create an event for every "to" address with the subject as the payload.

Event Example: SMTPd.receiver1@email.com 'This is the subject of the email'

A number of connected devices offer the ability to send an email in response to an event. This plugin will setup an SMTP mail server on the EventGhost system. You can configure your networked devices to send an email using the EventGhost IP as their mail server, and in response EG will fire off an event containing details of the incoming email. Now devices like IP cameras can send an event directly to EG via email.

Notes on useage
- When you add the plugin it will default to listen on 127.0.0.1 port 25. This will only allow local applications to send email to the   service. If you want to receive messages from external devices, set the address to your local network IP.
- You can change to port to a value other than 25, but first make sure all your other devices support a non-standard port.
- There is currently no support for SSL/TLS nor any sort of authentication. For this use case it doesn't really seem necessary.
- No emails will actually be delivered. Incoming messages will be received, an event triggered, and then disappear (this may change in the future).
