---
name: trace-meta
description: Audit your own Meta (Facebook/Instagram) data export. Counts tagged photos, off-Meta activity, advertisers and uploaded contacts; cites the source file for every number; gives cleanup steps.
---

TRACE · META — audit what Meta knows about you
Run it on your own Facebook / Instagram data export. Nothing leaves your machine.
Count only what is in the files. Cite the file path for every number. Never guess.

0 EXPORT  Accounts Center → Your information and permissions → Download your information. Format JSON, date range all time. Unzip to ./meta-export.

1 MAP  walk ./meta-export, list every folder and file with its size. Save MAP.md.

2 FACES  count photos and videos you are tagged in. Split posted-by-me vs uploaded-by-others; list the top uploaders by count and the years covered.

3 OFF-META  parse your activity off Meta technologies: every app and site, event count, first and last seen. Flag health, finance, dating and loan apps.

4 ADS  parse advertisers using your activity or information, plus ad interests and categories. Flag any inference about health, politics, religion or sexuality.

5 CONTACTS  count uploaded contacts and any call or SMS history in the export.

6 REPORT  write report.html: headline numbers, flagged items, a timeline. Every number links to its source file.

7 CLEAN UP  give me the exact steps to clear and disconnect off-Meta activity, delete uploaded contacts, and the removal form for family members who never had an account. Do not click anything for me.
