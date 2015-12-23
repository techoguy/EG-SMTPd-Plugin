# EG-SMTPd-Plugin
An Event Ghost plugin that uses SMTPd module to act as a basic SMTP server to trigger events in EG. 

Currently this plugin will simply create an event for every "to" address with the subject as the payload.

Event Example: SMTPd.receiver1@email.com 'This is the subject of the email'


The reason this plugin was created was that we wanted to be able to capture events from security cameras and security camera software to create what ever action we wanted. Most security cameras and software use an SMTP client to send emails and this is the only option to get events from these devices. So this plugin basically captures these emails from the cameras and creates events in EG which then can be used to trigger what ever EG will allow. 
