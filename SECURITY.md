[繁體中文](./SECURITY-zh_hant.md)，[简体中文](./SECURITY-zh_hans.md)

# Security Bounty Program
With a bounty program, we invite the software security community to research and discover security related bugs and vulnerabilities on Matters platform. 

If you would like to report a vulnerability or have a question for us, please email us at security@matters.news.


## Issues That Qualify

The following domains and assets are within the scope of the program:

- *.matters.news
- [public codebase](https://github.com/thematters) of Matters Lab, including Matters web app delivered via HTTP or IPFS

To be eligible, you must demonstrate a security compromise on any of these domains and assets using a reproducible exploit, for example:

- Cross-site scripting exploits
- Cross-site request forgery exploits
- Authentication or authorization flaws
- Official API flaws in rate and complexity limitation
- Server-side logic and code bugs
- Injection flaws
- Significant security misconfigurations


## Issues That Do Not Qualify

Below are some issues we have determined as not posing a great risk, or requiring systematic redesign of how our product works. They are not counted as valid vulnerabilities, but we still love to hear from you if you have any suggestions and comments.


1. Self-XSS.
2. CSRF/CORS configuration issue without a realistic scenario that can be exploited.
3. Registering multiple accounts for a single user.
4. Automation of certain actions such as like, commend or read article. 
5. Vulnerabilities in third party tools that utilizes Matters API.
6. Internal mechanism and logic of third party projects such as LikeCoin or IPFS


## We hope you: 


- Don’t make the bug public before it has been fixed.
- Don’t attempt to gain access to another user’s account or data. Use your own test accounts for cross-account testing.
- Don’t perform any attack that could harm the reliability/integrity of our services or data. 
- Do not impact other users with your testing, this includes testing for vulnerabilities in accounts you do not own. We may suspend your account and ban your IP address if you do so.
- Don’t use scanners or automated tools to find vulnerabilities. They create noise and extra pressure on our platform and we may suspend your account and ban your IP address.
- Don't carry out non-technical attacks such as social engineering, phishing, or physical attacks against our employees, users, or infrastructure.
- When in doubt, [email us](mailto:security@matters.news).


## And we will:


- respond as quickly as possible to your submission.
- keep you updated as we work to fix the bug you submitted.
- not take legal action against you if you play by the rules and act in good faith.
- give higher priority in both review and award for the submissions that are more thoroughly tested and demonstrated.



## Rewards

We will decide, at our sole discretion, the level of reward based on severity of the bug and completeness of the submission. The reward can be paid in LikeCoin (preferred) or US dollars.


### Critical: $500 (50000 LIKE)

Critical severity issues present a direct and immediate risk to a broad array of our users or to Matters itself. For example:


- SQL injecting into database
- bypassing login process and control a user’s account
- access to sensitive production user data
- access to internal production systems such as infrastructure management and operation support system
- accessing another user’s access token
- pay or withdraw from another user’s wallet

 
### High: $150 (15000 LIKE)

High severity issues allow an attacker to read or modify sensitive data that they are not authorized to access. They are generally more narrow in scope than critical issues, though they may still grant an attacker extensive access. For example:


- injecting attacker controlled content or code into matters.news webpages (XSS)
- bypassing scope control to gain more access than intended
- discovering sensitive user information in a publicly exposed resource
- gaining access to a non-critical resource that only Matters team should be able to reach

 
### Medium: $100 (10000 LIKE)

Medium severity issues allow an attacker to read or modify limited amounts of data that they are not authorized to access. They generally grant access to less sensitive information or more limited scope than high severity issues. For example:


- disclosing the title and content of a hidden article
- executing sensitive actions with another user’s session
- bypassing CSRF validation for low risk actions
- manipulating ranking and recommendation systems

 
### Low: Recognition on GitHub and Matters

Valid security vulnerabilities that don’t fall into the categories above or apply to auxiliary services and 3rd party dependencies. For example:
 

- unintentionally release of testing features
- bypasses size limitation on image upload or rate limitation on API request
- error not handled correctly without serious consequences

 

## Legal things & final notes

We deal only with principals, not vulnerability brokers.

If you reside in a country on a United States restricted export control list, or are on a United States state federal criminal wanted list or restricted export control list, you are not eligible to participate in this program.

We will make the final decision on bug eligibility and value. This program may be modified or canceled at any time, and any changes we make to these programs terms do not apply retroactively. Thanks for helping us make Matters more secure!