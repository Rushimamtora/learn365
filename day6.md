#  Cross-Site Leaks 

### [Goldmine to Learn](https://xsleaks.com/)


Index | Techniques
--- | ---
**1** | What is Cross-site Leaks
**2** | Cross-Site Oracle
**3** | XS-Search
**4** | Error Events 
**5** | Frame Counting 
**6** | Navigation Attacks
**7** | Cache Probing 
**8** | ID Attribute
**9** | Post Message Broadcasts
**10** | Abusing Browser Features
**11** | Timing Attacks
**12** | References

___
#### What is Cross-site Leaks
Cross-Site Leaks/XS-Leaks is a less explored security issue that usually comes from Side-Channel Attacks.\
This is an interesting vector but unusual.

```
This basically utilizes the web's core principle of composability in order to determine & extract useful information. 
XS-Leaks take advantage of small pieces of information that are exposed during interactions between websites.

```

#### Cross-Site Oracle
```
This can be considered as a querying mechanism. 
The information used for this attack is of binary form and called Oracles.
It usually has an answer of "Yes" or "No". You can say True or False.

Example

Does User Harsh Exists in the Application. 
Yes, means that the user is there in the application. 
An attacker requires to smartly form queries in order to successfully execute.
this attack and gain hold of sensitive information.

```

#### XS-Search
```
An attacker try to abuse the query mechanism such as search functionality to leak and get hold of the user's information. 

Remediation 
- Same Site Lax Cookies

Usual Exploitation Workflow: 

1. Define a timeline when there is a Hit vs Miss
2. Start attacking the Querying Endpoint. 
3. For Example: ?search=h (Throws a Hit)
search for the next word appended to `h` i.e. ?search=ha otherwise change the word i.e. ?search=b
```

#### Error Events 
```
Based on the Error Message returned by the application, it may be possible to enumerate sensitive information. 
This is similar to user enumeration techniques. 

```
https://hackerone.com/reports/505424

#### Frame Counting 
```
The window.length provides the number of frames in the window. 
This attribute can provide valuable information about a page to an attacker.

```
https://www.imperva.com/blog/facebook-privacy-bug/

####  Navigation Attacks

https://hackerone.com/reports/491473

#### Cache Probing 
```
Workes based on detecting whether the web page was cached or not.
```
https://terjanq.github.io/Bug-Bounty/Google/cache-attack-06jd2d2mz2r0/index.html

#### ID Attribute 
https://portswigger.net/research/xs-leak-leaking-ids-using-focus

#### Post Message Broadcasts
```
- Sharing Sensitive message with untrusted origins
- Leaking information based on varying content or on the presence of a broadcast
```

#### Abusing Browser Features 
```
- CORB (Cross-Origin Read Blocking)
- CORP (Cross-Origin Resource Policy)
```

#### Timing Attacks
```
- Clock Based 
- Network Timing
- Execution Timing
- Hybrid Timing 
- Connection Pool
```

####  References 
1. https://github.com/xsleaks/xsleaks/wiki/Browser-Side-Channels
2. http://sirdarckcat.blogspot.com/2019/03/http-cache-cross-site-leaks.html
3. https://medium.com/@terjanq/massive-xs-search-over-multiple-google-products-416e50dd2ec6
