Persona Chrome Extension (not really)
=====================================

I was hoping to integrate Persona and Chrome in a seamless experience. Instead
of having that ugly popup during login it would trigger a browser action popup
that looks more integrated with the browser.

Unfortunately Chrome doesn't allow the popup to be triggered from JavaScript:

http://stackoverflow.com/questions/10479679/how-can-i-open-my-extensions-pop-up-with-javascript


Another issue is that I wanted to inject my own script to define "navigator.id"
with my own polyfill (it's part of the BrowserID protocol). For some reason
script that runs on page load doesn't share the same namespace. Defining
navigator.id doesn't leak into the userspace as expected.

To be continued...
