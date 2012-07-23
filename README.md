NagiosCGI
=========

Nagios CGI Client (From: http://code.google.com/p/python-nagios/)

Why this fork?
--------------

The code.google.com version of python-nagios hasn't been touched since Sept, 2011. Additionally, it's feature incomplete and uncommented.

The aim of this fork is to add some needed features, touch up some existing methods, and add methods that are missing as needed.


How to use?
-----------

From http://exchange.nagios.org/directory/Addons/APIs/Python/python-2Dnagios/details 

**A library which allows you to interact with cmd.cgi.**
The cmd.cgi which comes bundled with Nagios has many abilities beyond acknowledging alerts, but writing software callouts for doing them can be tedious since the only documentation is the source code. Enter python-nagios, a library for interacting with cmd.cgi. It support both HTTP and HTTPS, passwords, and non-standard installation paths. A short example might be instructive:

    #! /usr/bin/env python
    import nagcgi
    cgi = nagcgi.Nagcgi("mon.example.com", "naguser", "nagpasswd", secure=True)
    
    cgi.add_host_comment('sillyhost', 'This host is being silly')
    cgi.disable_notification()
    cgi.ack_svc_problem('brokenhost','CHECK LOAD', 'running a highly parallel gcc build') 

