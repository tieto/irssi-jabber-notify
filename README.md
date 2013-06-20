irssi-jabber-notify
===================

My Jabber/XMPP notification script forked from @kreneskyp

This script now also supports GTalk(Hangouts) and other multi-domain
jabber services. If the server you connect to doesn't have the same
host name as your JID, then use the "xmpp_notify_domain" setting.
This will only work for as long as Google will support XMPP clients,
which is currently unclear.

If you are a Tieto user with a Google Apps account all you need to do is:
- put the script in ~/.irssi/scripts/ (or symlink from a git checkout)
- load it once: '/script load jabber_notify.pl' and
  - /set xmpp_notify_user firstname.lastname
  - /set xmpp_notify_pass applicationpassword 
    (NOT your domain PW, see https://support.google.com/mail/answer/1173270)
- now reload it:
  - '/script unload jabber_notify'
  - '/script load jabber_notify.pl'
- test if it works: '/xn-test' 
  (you should receive a message on all connected devices)

Please note, that some XMPP clients do not show messages from yourself.
One such client is telepathy on the Nokia N9/N950.

Peter's blog post:
http://blogs.osuosl.org/kreneskyp/2009/06/02/irssi-notifications-via-xmpp/
links the original:
http://staff.osuosl.org/~peter/myfiles/jabber-notify.pl

Side note:
If you are using bitlbee or some other way that can possibly make 
the notification messages come back to you, you might want to put
the notification sending JID on ignore to avoid a feedback loop.
