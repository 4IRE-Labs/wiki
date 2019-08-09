# Encoding seed phrase to the picture \(steganography\)

 **Challenge:** How might we ease up private key storing for cryptowallet users?

**End goal:** users can recover their private keys without the need to memorize or store them.

**Sprint Questions:**

* Can we make a seamless process on the mobile?
* How secure would be such a solution?
* How open are users for new options?

## Problem Research

![Customer Journey](../.gitbook/assets/image%20%2869%29.png)

### **Needs Hypotheses**

* User want easier backup of their seed phrases securely

### Existent Alternatives

* Write down the key/phrase
* Custodian approach
* Hard wallets integration
* Contacts Recovery \(Gnosis SAFE\)
* Knowledge Based Authentication
* Biometry

{% hint style="info" %}
Knowledge Based Authentication \(Steganography\) is comparably better than other alternatives
{% endhint %}

## Product Definition

A service/library that encodes the key into a picture/set of pictures at the wallet setup phase.

### Steganography

Visual cryptography is a cryptographic technique which allows visual information \(pictures, text, etc.\) to be encrypted in such a way that the decrypted information appears as a visual image.

The idea: Use image-based steganography and optional password to backup your seed phrase The rationale: The offline backup is proven to be fragile to a human factor errors. The hardware may crash. The ideal backup:

* is stored on many devices and cloud
* may be visible to public

There is only one asset that we all have that satisfies those conditions. Photo.

You may take a family picture that everybody has and encode your seed phrase with or without password. Send photo and feel safe.

### Prototype

![iOS App demo](../.gitbook/assets/img_8766.gif)

{% embed url="https://github.com/4IRE-Labs/CryptoGraphica" %}

## Test with users

Questions:

* How many crypto wallets you use?
* How do you store key phrases?
* How often do you recover?
* How convenient is it?
* Have you ever lost the they?

\*Test goes here\*

A library for wallets that allows saving the seed phrase into local stored photos

![Quick demo](../.gitbook/assets/img_8766.gif)

Repo: [https://github.com/4IRE-Labs/CryptoGraphica](https://github.com/4IRE-Labs/CryptoGraphica)

