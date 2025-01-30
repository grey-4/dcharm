![](https://grey-4.github.io/picture-repo/knightctf/2025-01-25_09-30.png)

Last week, Our team participated in the Knight CTF 2025. We placed 171th out of the 800 teams. Our team solved 14 challenges in which I contributed to 9 of them. This is also the ctf where I have solved most challenges.

---
# Osint 

## The Hidden Quest

Desc :

![](https://grey-4.github.io/picture-repo/knightctf/The%20Hidden%20Quest/2025-01-25_09-06.png)

As we can see, It is specified that the `secret` lies in somewhere in their recent posts.
Also If you if you read the first line it seems something intentional.

>The journey begins even before the battle starts!

This line hints that the secret has been revealed before the event. Searching for their social media I found that they had a facebook and twitter account from their contact us page.

Going through their posts before the event. I found 

![](https://grey-4.github.io/picture-repo/knightctf/The%20Hidden%20Quest/flag.jpg)

By zooming in , we can see the flag 

![](https://grey-4.github.io/picture-repo/knightctf/The%20Hidden%20Quest/flag_zoomed.png)

Flag : `KCTF{w0W_y0U_G07_m3_}`

# Networking 

## The Server's Identity 

Desc:

![](https://grey-4.github.io/picture-repo/knightctf/The%20Server%5C'%20s%20Identity/2025-01-29_13-33.png)

We were given an pcapng which can used with wireshark to analyse the packets. So After inputting the pcapng file. We can see that It has a lot of http requests. By the checking the first package itself and checking the data in it, We are able to make out the hostname.

![](https://grey-4.github.io/picture-repo/knightctf/The%20Server%5C'%20s%20Identity/sol.png)

Flag: `KCTF{localhost.localdomain}`

