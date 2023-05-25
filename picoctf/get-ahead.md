# GET aHEAD

This CTF involved an empty webpage with 2 options which changed the background colour of the page. The flag, however was not related to any of these functions...

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

Utilising Burp Suite, we can see the methods used for the buttons are GET and POST which is odd given the functionality is the same for both buttons.

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

We can also see GET is used to request the webpage.&#x20;

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

Changing this to POST yields no results...What happens if we change it the HEAD...We can finally see that changing the method to HEAD displays the headers of the page, including the flag.-

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>
