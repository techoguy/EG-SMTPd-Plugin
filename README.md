# EG-SMTPd-Plugin
An Event Ghost plugin that uses SMTPd module to act as a basic SMTP server to trigger events in EG. 

Currently this plugin will simply create an event for every "to" address with the subject as the payload.
Event Example: SMTPd.receiver1@email.com 'This is the subject of the email'
