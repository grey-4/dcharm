One day in our Discord server, my friend Drago threw me an OSINT challenge

“Try doing OSINT on this image.It’s not a CTF or anything serious — just something I found on a random webcam through Shodan.It’ll be good practice. I only need the country and village name,” Drago said.

![](https://miro.medium.com/v2/resize:fit:640/0*thmPBWiZoLkW5QBK)

The image

Curious, I took up the challenge. The image he shared didn’t have any obvious clues at first glance, but I was determined to figure it out. Here’s how I cracked it.

# The Clues I Found

- **Source on Shodan**: Since Drago said the image came from Shodan, I figured that reverse image searching might help, but unfortunately, the image’s metadata didn’t give me anything useful either.

![](https://miro.medium.com/v2/resize:fit:700/1*F07cwWlbOsQmjpZsiU6Ilw.png)

- **Looking for Clues in the Image**: The first thing I focused on were the **cars** in the driveway. I noticed two cars in the driveway:
- **Nissan Micra**
- **Mercedes-Benz C-Class Estate**

Both cars are popular in **Europe**, which helped me narrow down the region a bit.

- **License Plate Details**: Looking closer at the orange car’s license plate, I noticed it had a flag with **blue, white, and red** stripes. That left me with two main suspects: **France** or **the Netherlands**.
- **Shodan to the Rescue**: Knowing that Shodan tends to have more webcam images from the Netherlands than France, I focused my search there. I used this query:

has_screenshot:1 -screenshot.label:blank country:"NL"  Server:1

![](https://miro.medium.com/v2/resize:fit:700/1*zKKf4U7osUOdpEPS_BCAqw.png)

Image ratio of Netherlands and France in shodan

Boom! I got around 300 results. I sifted through them patiently, scrolling through one by one…

- **The Final Find**: And finally, I found it. The image came from a webcam located in **Waarde**, a small village in the Netherlands. Mission accomplished!

![](https://miro.medium.com/v2/resize:fit:700/1*lwP5SZBlkyRdnkN46wNgtg.png)

image on shodan

And that’s how I solved Drago’s OSINT challenge. Thanks for reading!