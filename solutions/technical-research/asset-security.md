# Improving Seed Phrase Storage Usability with Steganography

## Stakeholders

* Users
* Wallets \(incl. dapps, exchanges etc\)

## **Needs Hypotheses**

* **PRIO** Wallets want to improve usability of existent solutions \(not print\)
* User want easier backup of their seed phrases securely

### Existent Alternatives

* Hot wallet approach
* Hard wallets integration
* Contacts Recovery \(Gnosis SAFE\)
* Knowledge Based Authentication / Steganography
* Biometry

## Solutions Hypotheses

* Knowledge Based Authentication / Steganography is comparably better than other alternatives

### Steganography

Visual cryptography is a cryptographic technique which allows visual information \(pictures, text, etc.\) to be encrypted in such a way that the decrypted information appears as a visual image.

The idea: Use image-based steganography and optional password to backup your seed phrase The rationale: The offline backup is proven to be fragile to a human factor errors. The hardware may crash. The ideal backup:

* is stored on many devices and cloud
* may be visible to public

There is only one asset that we all have that satisfies those conditions. Photo.

You may take a family picture that everybody has and encode your seed phrase with or without password. Send photo and feel safe.

