## Natas Level 15 → Level 16
- Go to url: http://natas15.natas.labs.overthewire.org
    - User: natas15
    - Password: AwWj0w5cvxrZiONgZ9J5stNVkmxdk39J
- This time it only allows us to check the existence of a user, implying a blind-based SQL injection
    - While we can't log in to anything, we can ask for pieces of information that will give us the password
    - Luckily SQL has the perfect tool called LIKE BINARY
    - Giving it a quick test looks like it works
        - natas16" AND password LIKE BINARY "%a%
- We're going to want to script this one so we don't have to manually guess every character
    - This process can be slightly optimized by first finding what characters are part of the set, reducing the 62 character set
- Our script can be found in the Python file
- After running the Python script, we will obtain a password
    - Through this reduction, O(32^62) becomes O(62+32^25), where 25 is the new character set (acehijmnpqtwBEHINORW35690)!
    - WaIHEacj63wnNIBROHeqi3p9t0m5nhmh