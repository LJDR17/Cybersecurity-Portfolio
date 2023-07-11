---
description: Forensics
---

# hideme

This CTF first gave a png file:

<figure><img src="../.gitbook/assets/flag.png" alt=""><figcaption></figcaption></figure>

Upon opening this file within a hex editor, we can see that that there are some indicators that files are embedded in this image, the letters PK indicate a zip file is present and we can also see names of directories e.g. secret/flag.

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

Utilising a tool called binwalk, we can extract the files within the image which contains a directory called secret...

<figure><img src="../.gitbook/assets/Screenshot from 2023-07-11 14-30-52.png" alt=""><figcaption></figcaption></figure>

Within this directory there is a png file called flag which upon opening it, reveals the flag.

<figure><img src="../.gitbook/assets/Screenshot from 2023-07-11 14-32-38.png" alt=""><figcaption></figcaption></figure>
