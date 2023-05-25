# SOAP

For this CTF I was greeted with this page which contains 3 buttons which provide details on the corresponding organisations:

<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

When you click on a button a request is made with the url /data:

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

We can see there is an XML request which requests details of the element containing the button, and with this information we can conduct an XXE attack and find other files on the server, which essentially means we will need to inject malicious XML.

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

By inserting the malicious XML alongside the normal request we can obtain the relevant file we need...

Here, we're using an external entity, that can access local or remote content via a declared system identifier. The system identifier is assumed to be a URI that can be accessed by the XML processor when processing the entity, so in this case it is file:///etc/passwd. The XML processor then replaces occurrences of the named external entity with the contents accessed by the system identifier.

<figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

By sending this request the private data and flag is now exposed...

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

