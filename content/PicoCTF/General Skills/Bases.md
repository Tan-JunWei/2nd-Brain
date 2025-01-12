---
tags:
  - GeneralSkills
  - easy
  - base64
Creation Date: 
Last Date: 
References: 
draft: 
modified: 2024-09-05T23:06:02+08:00
---
## Challenge Description
![[PicoCTF Bases.png]]

Aha, a challenge dealing with bases! We have this string, with no other clue about how it has been encoded:

```
bDNhcm5fdGgzX3IwcDM1
```

For my past CTF challenges, it is quite a common occurrence for flags to be [[Base64]] encoded. Let's test the hypothesis. 

For encoding and decoding tasks, my go-to tool is [[CyberChef]], since it can analyse the string and recommend a decoding method as well. This functionality is useful for many challenges, including this one. 
### Decoding
![[PicoCTF bases 2.png]]

After entering the string as input, [[CyberChef]] actually recommended decoding the string from [[Base64]], which meant that the string was indeed [[Base64]] encoded. Doing this gave me the following output:

```
l3arn_th3_r0p35
```

>[!faq] PicoCTF Hint: Submit your answer in our flag format. For example, if your answer was 'hello', you would submit 'picoCTF{hello}' as the flag.
>
>We just have to wrap the decoded string with `pico{}` to get the flag.

> [!NOTE] Flag
> picoCTF{l3arn_th3_r0p35}