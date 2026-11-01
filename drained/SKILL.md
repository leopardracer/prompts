---
name: trace-drained
description: Scan your own photo library for screenshots that expose seed phrases, private keys, cards, passwords and 2FA codes. Runs OCR locally, masks every secret, lists which apps can read your photos, and gives cleanup steps.
---

TRACE · DRAINED — find the screenshot that can drain your wallet
Run it on your own Mac. OCR runs locally. Nothing is uploaded anywhere.
Never print a secret in full. Mask everything, for example "orbit v***** c***** … (12 words)".

0 SOURCES  my Photos library (~/Pictures/Photos Library.photoslibrary/originals, iCloud synced) plus ~/Desktop, ~/Downloads, ~/Documents. Ask me before reading any other folder.

1 MAP  count every image by folder, year and type (photo vs screenshot). Save MAP.md.

2 OCR  run text recognition on every image with macOS Vision (a small Swift or Python script) or tesseract if installed. No cloud APIs. Keep the text in memory, never write it to disk.

3 FLAG  mark every image that contains 12 or 24 words from the BIP-39 wordlist, a private key (64 hex chars), a card number that passes the Luhn check, CVV or expiry, passwords, 2FA backup codes, authenticator QR codes, passport, ID or bank details.

4 TABLE  file name, date taken, where it lives (iCloud, Recently Deleted, Downloads), type of secret, risk level. Masked only.

5 APPS  give me a checklist for my iPhone: Settings → Privacy & Security → Photos. For every app with Full Access, tell me if it really needs it or should be Limited / None.

6 WALLETS  ask me for my public addresses only, never a seed phrase. Show me how to check and revoke token approvals. If any seed phrase was found in a photo, tell me to move all funds to a brand new wallet whose seed exists only on paper, today.

7 REPORT  write report.html: what you found, what I deleted, what I still need to do. Do not delete anything without asking me first.
