# Read:18 Summary
## Ceasar Cipher
* is one of the simplest and most widely known encryption techniques. It is a type of substitution cipher in which each letter in the plaintext is
replaced by a letter some fixed number of positions down the alphabet
* The encryption step performed by a Caesar cipher is often incorporated as part of more complex schemes, such as the Vigenère cipher, and still has modern application in 
the ROT13 system. As with all single-alphabet substitution ciphers, the Caesar cipher is easily broken and in modern practice offers essentially no communications security.
* The Caesar cipher can be easily broken even in a ciphertext-only scenario. Two situations can be considered:
  * an attacker knows (or guesses) that some sort of simple substitution cipher has been used, but not specifically that it is a Caesar scheme;
  * an attacker knows that a Caesar cipher is in use, but does not know the shift value.
--------------------------------------------------------------------------------------------------------------------------------------------------------
## Cryptography
* `Cryptography` : the art and science of encrypting sensitive information, was once exclusive to the realms of government, academia, and the military. However, with 
recent technological advancements, cryptography has begun to permeate all facets of everyday life.
* Cryptography, or the art and science of encrypting sensitive information, was once exclusive to the realms of government, academia, and the military. However, with 
recent technological advancements, cryptography has begun to permeate all facets of everyday life.
* With the vast amounts of personal data circulating the Internet, it is more important now than ever before to learn how to successfully protect yourself from 
individuals with ill intentions.
* `Cryptography` : at its most fundamental level, requires two steps: `encryption` and `decryption`. The `encryption` process uses a cipher in order to encrypt 
plaintext and turn it into ciphertext. `Decryption`, on the other hand, applies that same cipher to turn the ciphertext back into plaintext.
* `Polymorphism` : is basically a cipher that changes itself with each use. Meaning that each time it is used, it produces a different set of results. So, if you
encrypted the exact same set of data twice, each new encryption would be different from the previous one.
* `Polymorphism` : is most commonly used in cipher algorithms to encrypt computers, software, and cloud-based information.
* `Obfuscation` : is defined as “The act of making something unclear, obscure, or unintelligible”. It means that, in order to transmit a secure message, you must hold
back some of the information required to understand the message.
* Which, by default, means it would only take one person with knowledge of the original message to divulge the missing pieces to the public.


### Why Does Cryptography Matter?
  * With cryptography, a specific key and numerous calculations are required. Even if someone knew the encryption method used, they wouldn’t be able to decrypt 
  the message without the corresponding key, making your information much more secure.
  * cryptographic algorithms that actively protect almost all of our personal data.

### Types of Cryptography :
  * 1. Hashing : Hashing is a type of cryptography that changes a message into an unreadable string of text for the purpose of verifying the message’s
  contents, not hiding the message itself.This type of cryptography is most commonly used to protect the transmission of software and large files where the
  publisher of the files or software offers them for download. The reason for this is that, while it is easy to calculate the hash, it is extremely difficult to 
  find an initial input that will provide an exact match for the desired value.
    * the most common hashing algorithms are MD5 and SHA-1, however due to these algorithm’s multiple weaknesses, most new applications are transitioning to the SHA-256
    algorithm instead of its weaker predecessors.
    
  * 2. Symmetric Cryptography  : Symmetric Cryptography, likely the most traditional form of cryptography, is also the system with which you are probably 
  most familiar. This type of cryptography uses a single key to encrypt a message and then decrypt that message upon delivery.
    * Since symmetric cryptography requires that you have a secure channel for delivering the crypto key to the recipient, this type of cryptography is all but 
    useless for transmitting data (after all, if you have a secure way to deliver the key, why not deliver the message in the same manner?)
  ***Most modern symmetric cryptography relies on a system known as AES or Advanced Encryption Standards.***
  
  * 3. Asymmetric Cryptography uses two different keys for encryption and decryption, as opposed to the single key used in symmetric cryptography.
    * The first key is a public key used to encrypt a message, and the second is a private key which is used to decrypt them. The great part about this 
system is that only the private key can be used to decrypt encrypted messages sent from a public key.
    * While this type of cryptography is a bit more complicated, you are likely familiar with a number of its practical applications.
  * 4. Key Exchange Algorithms
  * 5.The 4 Types of Cryptographic Functions
    * Authentication 

    * Nonrepudiation : This concept is especially important for anyone using or developing financial or e-commerce applications.



    * Confidentiality : With information leaks and a seemingly endless number of privacy scandals making the headlines, keeping your private information,,
    well, private is probably one of your biggest concerns. This is the exact function for which cryptographic systems were originally developed.  


    * Integrity : Another important use of cryptography is to ensure that data is not viewed or altered during transmission or storage.

  * 6.Cryptography for the Everyday 
  * 7.it is necessary to ensure the continued security of your personal information. And with the rapidly evolving landscape of modern data, this topic
  is more important now than ever before.

  







 





































