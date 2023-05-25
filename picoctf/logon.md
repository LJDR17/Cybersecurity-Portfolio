# logon

This CTF first starts with a form element...

<figure><img src="../.gitbook/assets/image (9) (1) (1).png" alt=""><figcaption></figcaption></figure>

...However entering any details would prove unsuccessful at solving this one.

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

Utilising Burp Suite we can see that a new request has been made called flag which is the request we had just made to try and login. We can see there is a cookie with an admin field which is set to false...

<figure><img src="../.gitbook/assets/image (3) (2).png" alt=""><figcaption></figcaption></figure>

Upon setting this field to true and sending a request, we are finally met with the flag.

<figure><img src="../.gitbook/assets/image (4) (1).png" alt=""><figcaption></figcaption></figure>
