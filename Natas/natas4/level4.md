## Natas Level 4 → Level 5
- Go to url: http://natas4.natas.labs.overthewire.org
    - User: natas4
    - Password: Z9tkRkWmpt9Qr7XrR5jWRkgOU901swEZ
- The text says that we’re visiting from “”, while authorized users should come from http://natas5.natas.labs.overthewire.org/
- If I refresh, text says that we’re visiting from http://natas4.natas.labs.overthewire.org/, while authorized users should come from http://natas5.natas.labs.overthewire.org/
- It seems like the page detects where the user is coming from and it must be http://natas5.natas.labs.overthewire.org/
    - Probably using the Referer header, so we need something to edit that
- By using the burp suite, it is possible to intercept the packet and edit the Referer header field to have it appear to come from http://natas5.natas.labs.overthewire.org/
- Now the page displays the password
    - iX6IOfmpN7AYOQGPwtn3fXpbaJVJcHfq