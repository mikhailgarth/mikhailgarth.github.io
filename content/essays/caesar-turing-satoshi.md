---
title: "Caesar, Turing and Satoshi"
date: 2026-09-12T21:04:45-04:00
draft: false
description: "A brief overview of symmetric and asymmetric cryptography as practised by myself, Caesar, Turing and Satoshi."      # 150-160 char meta description for Google — write this deliberately, don't leave it blank
caseno: ""             # optional dossier-style file number, e.g. "07" — leave blank to hide
weight: 960             # controls display order: lower numbers appear first. Space essays out (10, 20, 30...) so you can slot new ones in between later without renumbering everything.
---
Bitcoin, Solana and Avalanche and Seed Phrases

I hold cryptocurrencies such as Bitcoin, Solana and Avalanche partly as a hedge against inflation and partly because I have a libertarian streak which makes me fantasize that I can be independent of traditional finance and the moguls of Wall Street.  I do not keep them on an exchange because part of my libertarian idea is that I should control the cryptocurrency assets and not the exchange.  Of course, this means that I am completely responsible for their safe-keeping and I cannot blame an exchange if they disappear.

For this self-custody, I set up wallets using a 12 or 24 word seed phrase, and then send my crypto assets to them through the corresponding public addresses.

These seed phrases are the key to my own little slots on the blockchains where I keep digital representations of my assets. The seed phrases are all that stand between my precious assets and the big wide threatening universe.  This universe is inhabited by unsavory individuals who work relentlessly to separate me from my assets.  They can work from their mothers’ basements or from the seediest areas of third world cities.  They could even work for subversive foreign agencies.  They use phishing, malware, false websites and even false mailings for their nefarious purposes in order to separate me from my seed phrases.

My only defense is to not keep my seed phrases on my computer or phone but instead write them on paper, etch them in steel or commit them to memory.  I can also spread the assets out over many different wallets, only access them from one dedicated laptop which I do not use for any other purpose, and, above all, keep my mouth shut about them. I realize I have just broken that rule but hope I have been sufficiently vague so that it does not matter.  It seems that the person who understands the risk best is sometimes the one who breaks the rule.

Asymmetric Cryptography

It is fascinating to me that I cannot work my way back from the public addresses to derive the seed phrases.  You do not need to know my seed phrase in order to send me crypto tokens or coins.  You can send assets to my slot on the blockchain and you can see what it contains (with most but not all blockchains) using my public address but you cannot help yourself to the contents of my slot. For this, you need the seed phrase.  And only I know the seed phrase if I am careful.

This is called asymmetric cryptography because the method used to encrypt access to the slot on the blockchain (the public key) is not the same as the method used to decrypt it (the private key).  In asymmetric cryptography you have two mathematically linked keys — one that locks, one that unlocks but crucially, knowing the locking key tells you nothing useful about the unlocking key.

This was a revolutionary idea. Every system before it required both parties to already share the same secret: symmetric cryptography.  Asymmetric cryptography solved the problem that had plagued cryptography for two thousand years: how do you establish a secret with someone you have never met?

It is as if you buy a padlock and send it — unlocked, open — to anyone who wants to send you something. You keep the key yourself and never share it with anyone.

•	Anyone can snap the padlock shut on a box containing their message

•	Only you can open it, because only you have the key

•	Someone intercepting the padlock in transit gains nothing — it is open and empty

•	Someone intercepting a locked box gains nothing — they have no key

Your public key is the open padlock — share it with the entire world. Your private key is the key to that padlock — never let it leave your possession.

Julius Caesar and Symmetric Cryptography

Compare with Julius Caesar’s method of cryptography.  It was simple substitution so that he represented each letter with, for example, the third letter after that in the alphabet.  This is symmetric cryptography because the same method is used to both encrypt and decrypt a message.  
Caesar's cipher was completely reversible with equal effort in both directions. If you knew the method and had the ciphertext, decrypting was just as easy as encrypting.

Modern cryptography is built on one-way mathematical functions — you can go one way but not the other.

Caesar’s cipher is easy to break because frequency analysis can be used.  In any language, certain letters appear far more often than others. In English, E is the most common letter, followed by T, A, O, I, N.  If you intercept a Caesar-encrypted message long enough, you can simply count which encrypted letter appears most often — that is probably E — and work backwards to find the shift. Caesar's cipher falls to this attack in minutes. 

The Enigma Cipher

In the middle of this progression from Caesar’s cipher to crypto, we have Enigma.

Enigma was better than Caesar’s cipher because the substitution changed constantly.  Caesar used one fixed substitution throughout an entire message. Enigma's rotors advanced with every keypress, meaning each letter was encrypted with a completely different substitution than the one before it.
Press A three times in a row and you might get X, then Q, then M. The same letter never reliably produced the same output twice. This removed the main weakness of Caesar — frequency analysis.  The number of possible Enigma configurations — which rotors, which order, which starting positions, which plugboard settings — ran to approximately 158 quintillion combinations. The Germans were supremely confident this made it unbreakable.

The Origins of Enigma

Enigma was invented by Arthur Scherbius, a German electrical engineer, who patented the design in 1918 — just as the First World War was ending. His motivation was commercial. He saw a market for secure business communications where competitors or criminals could not read them.
The British and Americans examined commercial Enigma machines in the early 1920s and found them too cumbersome and expensive for practical military use.

The German military began adopting Enigma in the late 1920s and through the 1930s.  They made significant modifications that made it more secure than anything Scherbius had originally sold. Also, different branches of the German military adopted different versions.

The Polish Cipher Bureau and Enigma

Alan Turing is the British mathematician most closely associated with breaking the Enigma cipher during the Second World War.  However, the Polish Cipher Bureau broke Enigma in 1932, seven years before the war began, and Turing knew this.

When Germany invaded Poland in September 1939, the Polish Cipher Bureau passed everything they knew to British and French intelligence in a secret meeting in the Warsaw woods. Turing and his colleagues at Bletchley Park inherited this foundation and built upon it.  They did not start from nothing but the Poles rarely get the credit.  Sometimes, it is the leader who builds on prior work who takes the glory.

Turing and Enigma

Turing did not break Enigma by brute force: trying all 158 quintillion combinations was as impossible then as guessing your seed phrase is today.  If you could test one Enigma setting every second, checking all 158 quintillion combinations would take about 5 trillion years.  This is several hundred times longer than the current age of the universe.  Instead, he exploited the weaknesses in how humans used the machine.

The critical weakness was this: Enigma could never encrypt a letter as itself. A could never become A. B could never be B.

Enigma's entire purpose was to produce output indistinguishable from random noise. But a truly random substitution would occasionally map letters to themselves. Enigma never did.

This means anyone who knew this property could immediately distinguish Enigma output from true random noise, which is what you should never be able to do with a well-designed cipher.  This fatal flaw was there from day one but went unexploited for years until Turing understood what to look for.  Sometimes, the flaw you are most exposed to is the one you do not notice because it has always been there, not a new external threat.

In modern cryptographic terms this violates a fundamental security requirement. A secure cipher must produce output that is computationally indistinguishable from random. Enigma failed this test by design, structurally, on every single character encrypted.

German operators also followed predictable habits:

•	Weather reports always began with the word WETTER (weather)

•	Messages often started with KEINE BESONDEREN EREIGNISSE (nothing to report)

•	Officers frequently sent messages beginning with HEIL HITLER

These predictable phrases were called cribs — known or guessed pieces of plaintext. Turing's Bombe machine used cribs to dramatically narrow the search space, ruling out vast numbers of impossible configurations almost instantly.  Turing’s task could have been made much more difficult if the Germans had had the foresight and discipline to avoid using these cribs.  There was vulnerability both in the design and in the people. 

Satoshi and Bitcoin and Proof-Of-Work

Asymmetric cryptography was invented in the 1970s but Satoshi’s contribution was to solve a problem that had stumped digital currency proposals for years before Bitcoin: how do you stop the same digital token from being spent twice without a bank or central authority checking a ledger and verifying the transaction?  This is the famous double-spending problem.

This is not an issue with physical cash because when you give somebody a dollar bill, you no longer have it.

Satoshi combines several existing pieces:

1.	Public-key asymmetric cryptography that we described earlier

2.	Blocks to contain digital tokens chained together on the internet in multiple nodes on the internet

3.	‘Miners’ competing to solve a computationally expensive puzzle to add the next block in the chain in return for a reward of more digital tokens for proof-of-work

4.	The longest valid chain is treated as the truth because it contains the most accumulated computational work and all other nodes have to synchronize and match it

If somebody wants to spend the same digital token twice, they have to go back and change one of the blocks.  This requires redoing the proof-of-work for every subsequent block faster than the rest of the network so they can get ahead of all the unchanged nodes – the famous 51% attack threshold.  Cheating is theoretically possible but irrational since you would need more computing power than everybody else.

Failures with Bitcoin and other cryptocurrencies and blockchains have come from human and implementation flaws: lost seed phrases, exchange hacks such as Mt.Gox, exploited smart contracts or 51% attacks on smaller blockchains.   Bitcoin’s proof-of-work has never been broken mathematically at all, so far.

How Different Cryptography Methods are Vulnerable

The three cryptography methods we have discussed are all vulnerable to human weaknesses.

Caesar’s letter shifting cipher could be broken by frequency analysis.  Enigma could be broken because it was not truly random and you could detect predictable phrases.  Bitcoin and other blockchains can be compromised by stolen seed phrases.

It is a testimony to the strength of asymmetric cryptography that the only way private keys in blockchains can be broken is when the human fails to guard the seed phrase (at least until quantum computing develops). This is why shady characters send emails screaming that I need to update my hardware wallet now or all will be lost or that I only need to click on the link in this email to find untold riches.  No matter how complex the mathematics, humans can always give away the secret.