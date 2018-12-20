# Wording

## **An update on this issue.  Not just .. but. Not only.. but. seems to be**

> An update on this issue** (I'm having the same problem with high CPU usage when Flow and Firefox are running): **first**, **although** it's not explained anywhere in the documentation from HP, **here's** a little about what Flow does: it's supposed to monitor what the computer is doing and adjust the audio mode to that. So if you're playing a movie, the audio is in movie mode, music mode for music, etc. So it tries to monitor what the user is doing, **not just** what programs are running **but** what they're doing. For example, it tries to watch **not only** what site a browser (e.g., Youtube) is on **but** what kind of video it is (e.g., with a music video, it goes to music mode).
>
> The problem **seems to be** with recent versions of Firefox that Flow isn't able to properly monitor. It seems to be trying repeatedly to communicate with Firefox and not properly reading what it's doing. I tried with Edge, which seems to be fine: switching between a music video and a lecture switches the mode from music to voice, and there's no CPU usage issue. It spends a lot of CPU time whenever a new tab is opened (meaning, presumably, that a new Firefox process is spawned), because however it was trying to access the information isn't working and it's spending a lot of time at it before giving up. And Firefox is apparently also using a lot of CPU cycles trying to respond to its requests.
> So this needs to be fixed either by changing how Flow communicates with Firefox or by having it not even try to read Firefox's state.

## **Prevent, designed to, it is intended to, to be scalable**

> The CPE WAN Management Protocol **is designed to** provide a high degree of security.
> The security model is also designed to be scalable. **It is intended** to allow basic security to accommodate less robust CPE implementations, while allowing greater security for those that can support more advanced security mechanisms. In general terms, the security goals of the CPE WAN Management Protocol are as follows:
>
> - Prevent tampering with the management functions of a CPE or ACS, or the
> - transactions that take place between a CPE and ACS.
> - Provide confidentiality for the transactions that take place between a CPE and ACS.
> - Allow **appropriate** authentication for each type of transaction.
> - **Prevent** theft of service.

## **Pros, Cons, In Summary**
> **HTTP Basic Access Authentication**
>
> - *STEP 1* : the client makes a request for information, sending a username and password to the server in plain text
> - *STEP 2* : the server responds with the desired information or an error
>
> Basic Authentication uses **base64** encoding(not encryption) for generating our cryptographic string which contains the information of username and password. HTTP Basic doesn’t need to be implemented over SSL, but if you don’t, it isn’t secure at all. So I’m not even going to entertain the idea of using it without.
>
> *Pros:*
>
> - Its simple to implement, so your client developers will have less work to do and take less time to deliver, so developers could be more likely to want to use your API
> - Unlike Digest, you can store the passwords on the server in whatever encryption method you > like, such as bcrypt, making the passwords more secure
> - Just one call to the server is needed to get the information, making the client slightly faster than more complex authentication methods might be
>
> *Cons:*
>
> - SSL is slower to run than basic HTTP so this causes the clients to be slightly slower
> - If you don’t have control of the clients, and can’t force the server to use SSL, a developer might not use SSL, causing a security risk
>
> *In Summary* – if you have control of the clients, or can ensure they use SSL, HTTP Basic is a good choice. The slowness of the SSL can be cancelled out by the speed of only making one request

；