# node-red-contact-form-examples #

contact and user feedback flows for Node-RED

Often web sites offer visitors the possibility to contact the web page operator. This is usually achieved by means of a specific web page containing a feedback form and a button to submit the form contents.

This repository contains two examples for such an approach:

* the first one (called "User Feedback") assumes that users visiting the feedback page can be trusted, e.g., because they had to authenticate themselves before. As a consequence, there is no kind of captcha or similar mechanism to detect bots which try to submit SPAM through this form.
* the second one (called "Contact Form") does not make such an assumption - but it also avoids captchas, which often turn out not to be GDPR compliant. Instead, the first visit of the contact page creates a time-based token which gives the visitor a time slot ranging from 1 to 15 minutes after the first visit to submit a message - and this exactly once. Practice shows that waiting 1 minute before being able to submit a message overtaxes bots and daunts human spammers. 

> Nota bene: this work is currently in progress, do not expect it to be finished before end of October 2021

> Just a small note: if you like this work and plan to use it, consider "starring" this repository (you will find the "Star" button on the top right of this page), so that I know which of my repositories to take most care of.

## Prerequisites ##

Both examples require the following Node-RED extension

* [node-red-contrib-reusable-flows](https://github.com/rozek/node-red-contrib-reusable-flows)<br>"Reusable Flows" allow multiply needed flows to be defined once and then invoked from multiple places
* [node-red-node-email](https://github.com/node-red/node-red-nodes/tree/master/social/email)<br>contains Node-RED nodes to send and receive simple emails

## User Feedback (without Token) ##

![](user-feedback.png)

## Contact Form (with Token) ##


## License ##

[MIT License](LICENSE.md)
