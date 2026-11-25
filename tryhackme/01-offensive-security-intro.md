# Room 1: Offensive Security Intro

**Date:** 2026-11-24
**Link:** https://tryhackme.com/room/offensivesecurityintro
**Time spent:** 5 minutes

## What I learned
- Offensive security means thinking like an attacker to find weaknesses before a real attacker does.
- Hidden pages and directories can be discovered by guessing common names from a wordlist.
- Once a hidden path is found, you add it to the site's URL to open that page.

## Tools and commands
- `dirb http://target-url`: tries paths from a wordlist against a site and reports the ones that exist.

## Key terms
- **Wordlist:** a file of common names (like admin, login, backup) used for guessing.
- **Directory brute-forcing:** trying many paths to find ones that aren't linked anywhere.

## Questions I still have
- How do defenders detect this kind of scanning?

## Next
Room 2: Defensive Security Intro
