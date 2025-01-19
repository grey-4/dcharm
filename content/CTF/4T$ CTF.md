![](https://miro.medium.com/v2/resize:fit:700/0*8HyaHpgQEZ8jiqkw)

Recently, I participated in the 4T$ CTF (albeit at the last minute). I started by looking for challenges with fewer points (easy ones) since I didn’t have much time left in the event.

I decided to tackle the OSINT challenges, as they had more solves than the others — and, of course, OSINT is fun!

# **Challenge 1 : Hoot Hoot**

Description :

> Hello Agent,
> 
> We are looking to locate a wanted person. We have obtained a photo that may be near their residence. Could you find the name of the city for us? Thank you.
> 
> The name of the city must be in lowercase, without accents, and without spaces
> 
> The flag is in this format: `4T${<city>}`. If the solution were New York, the flag would be `4T${newyork}`.

Resource given :

![](https://miro.medium.com/v2/resize:fit:256/1*P4UjTuQUZ6YvXhBXwoHLZA.png)

hoothoot.png

To identify the city where the photo was taken, I first checked for any metadata embedded in the image using

exiftool hoothoot.png

After checking the metadata

![](https://miro.medium.com/v2/resize:fit:694/1*rmaBvGKBT1luHLyKx40hXw.png)

result1.png

I decided to put the image into Google Lens, as architectural structures are usually recognizable.

![](https://miro.medium.com/v2/resize:fit:540/1*2IdnQI_a1yIKoYelu_SH9Q.jpeg)

solution1.jpg

It worked, and I found the solution for the first challenge

Solution : 4_T${dijon}_

# **Challenge 2: Targets**

Description :

> Hello Agent,
> 
> You are doing a great job. We have contacted the local authorities to gather information on our target.
> 
> We have since discovered that our target is part of an activist group called Hackcorp. They are planning an attack on three locations. For several years, our target has been gathering information on these locations.
> 
> Attached, you will find three photos of potential locations. You must identify the positions of these locations.
> 
> The location we ask you to find are:
> 
> First picture: It is pretty obviuous…
> 
> Second picture: The building on the center of background.
> 
> Third picture: The building where the photo was taken.
> 
> The flag is the concatenation of the first word of each three word.
> 
> The flag is in this format: `4T${word1.word2.word3}`

Resource given :

![](https://miro.medium.com/v2/resize:fit:700/1*zfnft5iJL7a5-7LQMVjDiA.png)

Target1.png

![](https://miro.medium.com/v2/resize:fit:700/1*6bByLnuxvB358RYkWU1YFA.png)

Target2.png

![](https://miro.medium.com/v2/resize:fit:700/1*L4kGlfRYK9uA-u_dooZNOg.png)

Target3.png

Following protocol, I checked the metadata of each image to see if there were any embedded clues

> Note : Metadata checks before reverse imaging can be helpful in CTFs, as sometimes we overlook the clues within them.

exiftool Target1.png  
exiftool Target2.png  
exiftool Target3.png

![](https://miro.medium.com/v2/resize:fit:700/1*nlu2QNwh1IgKy8NQNqWnrw.png)

Target1_md.png

![](https://miro.medium.com/v2/resize:fit:700/1*ZBVg4fjUTYOQH7EE2gpPvA.png)

Target2_md.png

![](https://miro.medium.com/v2/resize:fit:700/1*9AjQK7EBR9Zet1BAFNoKjg.png)

Target3_md.png

After verifying that there were no hints in the metadata, I moved on to reverse image search for each picture.

**Target1 :**

Google Lens identified the location as

![](https://miro.medium.com/v2/resize:fit:540/1*mtbwYM7UdwTpz7Fs_gxEoA.jpeg)

Solution_1.png

The location of the image has been found

solution : _Le char Duguay-Trouin_

**Target2 :**

This one was trickier. The task was to locate the building in the center of the image.

Lens helped identify the tracks in the image,

![](https://miro.medium.com/v2/resize:fit:700/1*24mzcgK6TfxM2kvl7m7nug.png)

map

so I switched to Street View to narrow it down.

![](https://miro.medium.com/v2/resize:fit:700/1*KKDwKbKgcWrQt996ECS6fQ.png)

street view

Eventually, I found the answer

![](https://miro.medium.com/v2/resize:fit:700/1*a7ZkVwnRtNF1llZK9licnA.png)

solution_2.png

Solution: _Crypte de Saint-Bénigne_

**Target3 :**

Target3 had no obvious visual clue to trace back to the location. However, there were a couple of subtle hints:

- _It’s a sushi restaurant._
- _All the previous locations were in Dijon._

Based on these hints, I began searching for Japanese cuisine restaurants in Dijon. While browsing the review photos, I found a match: _Koki Dijon_, with windows, wooden pillars, plate styles, and metal trays that aligned perfectly.

![](https://miro.medium.com/v2/resize:fit:675/1*BRbBJ3vf3BFmgN9azH7EqA.png)

solution_3.png

So At this point we can confirm this is the location

Solution : _Koki Dijon_

**Flag Format :**

Many may fail here, Because they did not notice the hinting in this sentence

> The flag is the concatenation of the first word of each three word.

The each three word here means [what3words.com](https://what3words.com/toddler.geologist.animated)

By inputting

- Le char Duguay-Trouin
- Crypte de Saint-Bénigne
- Koki restaurant, Dijon

in What3places. I got

- intro.singled.spines
- smoke.sizzled.warnings
- farmer.cheaply.splendid

These are the actual answers.

By concatenating the first word of each we will get

Solution : _4T${intro.smoke.farmer}_

# Conclusion:

Overall, the 4T$ CTF was a great experience, especially diving into OSINT challenges under pressure. Even though I joined at the last minute, I enjoyed tracking down clues, piecing things together, and seeing the strategies pay off. It was a fun, quick test of skills — and definitely worth it!

Follow for more!