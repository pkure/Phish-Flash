# Phish Flash 🎴
 
**A free, browser-based game that trains anyone to spot phishing and social engineering - by getting reps.**
 
🔗 **Live:** [phish-flash.com](https://phish-flash.com) &nbsp;·&nbsp; 💛 Free, no sign-up &nbsp;·&nbsp; 🛡️ Safe by design &nbsp;·&nbsp; 🤖 AI-assisted, human-reviewed
 
---
 
![Phish Flash main screenshot](assets/main-mockup.png)
 
> *Hero banner: Phish Flash on a phone and laptop side by side, one card mid-flip. Alternative: logo on brand gradient.*
 
---
 
## The problem I'm trying to solve
 
Phishing used to be easy to laugh at - the misspelled words, the lottery you never entered, the obvious graphics and butchered logo images. It isn't anymore. AI now writes flawless, personalized lures at scale, clones brands pixel-for-pixel, and stands up convincing fake login pages in minutes. The people most exposed to this - older relatives, busy non-technical folks, anyone who didn't grow up online - are often the least equipped to keep up.
 
I built Phish Flash because I believe the defense has to scale the same way the attack does: through practice. You don't learn to spot a fake by reading a checklist once. You learn it the way a SOC analyst does - by seeing hundreds of real-shaped examples until the tells jump out at you. Phish Flash turns that into a fast, friendly flashcard game that's free and open to everyone, whatever their age or technical skill.
 
---
 
## How it works
 
The landing page is the game. You're shown a message - an email, a text, a login page, a voicemail - and you decide: **legit or malicious?** Then you flip the card. The exact tells light up, and a plain-language breakdown explains what gave it away and how to check it yourself using free tools anyone can use - no jargon, written for a non-technical reader.
 
No score, no sign-up, no pressure. Just reps: land → decide → flip → learn → next.
 
---
 
![The core loop ](assets/card-flip-demo.png)
 

---
 
## What I built
 
This is a real, shipped, self-hosted product - not a tutorial clone. A few things I'm proud of:
 
### AI-assisted content, with a human always in the loop
 
New cards are generated from modern, real-world threat patterns - but every single card is reviewed and approved by a human before it can go live. The automated generator can only ever write to a review queue; it can never publish on its own. AI gives me volume and freshness; the human gate keeps every card accurate, safe, and genuinely educational. To me that's the responsible way to use AI for security content, and it's built into the architecture rather than bolted on.
 
### A real CI/CD pipeline
 
Every change runs through automated quality and security gates (via GitHub Actions) before it can ship, and deployment is a scripted, repeatable pipeline rather than a manual copy. For a site that displays simulated phishing, having those checks stand between a change and the live site matters a lot.
 
### Safety-first by design
 
This is the constraint I care about most. Every card is completely inert - no working links, no live code, nothing that could harm a visitor or get the site itself flagged. The simulated "attacker" domains, emails, and phone numbers are all invented and fictional. I'd rather under-build than ship anything that could hurt the people I'm trying to protect.
 
### Self-hosted, end to end
 
I run the infrastructure for this myself - domain, server, deploys, and monitoring. It's mine to keep alive.
 
---
 
![Pipeline diagram](assets/pipeline-diagram.png)
 
 
---
 
## Stack
 
| Layer | Tech |
|---|---|
| Frontend | Next.js, Tailwind CSS |
| Content pipeline | AI-assisted generation (Claude), human review queue |
| CI/CD | GitHub Actions |
| Hosting | Self-hosted |
 
---
 
## Free, and built for everyone
 
There's no paywall, and there never will be. The whole point is reach: the people who most need this are the least likely to pay for security training, so it has to be free and approachable. Explanations are written in plain language for a smart non-technical reader, it works great on a phone, and you can start learning in a few seconds without making an account.
 
---
 
## Contributions & submissions
 
Seen a phish in the wild? Have an idea for a scenario? We welcome submissions. You can send:
 
- 📷 Screenshots / images of a suspicious message (with personal details removed)
- ✍️ Descriptions of a scam or tactic you've run into
- 🧩 Suggestions for new card templates or themes you'd like to see
Send it to [info@phish-flash.com](mailto:info@phish-flash.com) and it may become a card others learn from.
 
> Please strip anything personal or identifying before sending - we only need the tactic, never your data.
 
---
 
## Contact
 
[info@phish-flash.com](mailto:info@phish-flash.com) &nbsp;·&nbsp; [phish-flash.com](https://phish-flash.com)
 
---
 
<details>
<summary>A note on brands shown here</summary>
Phish Flash is a security-awareness training simulation. Real company and brand names or logos may appear, but only ever as the *impersonated target* of a fictional attacker - shown so people can learn to recognize real-world impersonation. We never imply that any real company, brand, or domain is itself malicious, compromised, or untrustworthy. Every domain, email address, and phone number used by the imaginary attackers is invented and fictional. If you represent a brand shown here and feel the portrayal is unfavorable, please contact us via [phish-flash.com](https://phish-flash.com) and we'll gladly change or remove the reference.
 
Every scenario is a fictional, illustrative example; all links are inert. Nothing here is professional, legal, or security advice. Provided "as is."
 
</details>
