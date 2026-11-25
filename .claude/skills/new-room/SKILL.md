---
name: new-room
description: Creates the next blank TryHackMe room note in this cyber-notes repo (e.g. tryhackme/03-careers-in-cyber.md) from the user's standard template, numbered and named like the existing rooms, and adds it to the README checklist. Use this whenever the user asks to make, create, add, start or set up a new room, the next room, a room file or a blank template, or says something like "new room: Careers in Cyber" or "set up room 3", even if they don't say "skill".
---

# New room

The user writes their own notes for each TryHackMe room. This skill only sets up the blank file so they don't have to copy the template by hand. Don't fill in what they learned, terms, questions or anything else from your own knowledge. The sections stay empty for them to write.

## 1. Work out the room number and name

- Look in `tryhackme/` for files named `NN-some-name.md`. The new room's number is the highest `NN` plus one, written with two digits (`03`, `04`, … `10`).
- **Name:** use the one the user gave. If they didn't give one, read the `## Next` section of the latest room. It usually names the next room (for example "Room 3: Careers in Cyber"). If it's empty or unclear, ask for the name.
- If the user names a specific number (like "room 5"), use that number. If a file with that number already exists, stop and ask. Never overwrite a note.

## 2. Create the file

**Path:** `tryhackme/NN-room-name.md`, where the name is lowercase with hyphens and words like "Intro" are kept. For example, "Careers in Cyber" becomes `tryhackme/03-careers-in-cyber.md`.

**Content:** use this template exactly. Only the title, date and link get filled in.

```markdown
# Room N: <Room Name>

**Date:** <today's date, YYYY-MM-DD>
**Link:** <room URL>
**Time spent:** 

## What I learned
- 

## Tools and commands
- 

## Key terms
- **Term:** 

## Questions I still have
- 

## Next

```

- The title number has no leading zero: the file is `03-…` but the title is `# Room 3: …`.
- **Link:** TryHackMe room URLs look like `https://tryhackme.com/room/<slug>`, where the slug is usually the room name in lowercase with no spaces (for example `careersincyber`). Fill it in only if the user gave the URL or you're confident of the slug. Otherwise leave it as `**Link:** ` for them to paste.

## 3. Add it to the README

The README has a checklist under the TryHackMe heading, like:

```markdown
## TryHackMe: Pre-Security
- [x] [Room 1: Offensive Security Intro](tryhackme/01-offensive-security-intro.md)
- [ ] Room 2: Defensive Security Intro
```

- If the room is already listed, turn its text into a link to the new file and leave the checkbox as it is.
- If it isn't listed, add `- [ ] [Room N: Name](tryhackme/NN-room-name.md)` at the end of the list.
- **Tick off the previous room.** Starting a new room means the user finished the one before it, so change its `- [ ]` to `- [x]`. If that line isn't linked yet, turn it into a link to its file in `tryhackme/` as well.
- Leave the other lines as they are. If an older room (not the one just before) is still unticked or unlinked, mention it in your reply and offer to fix it rather than changing it yourself.

## 4. Reply

Keep it short: link the new file, say which room you ticked off, say whether the Link field was filled in or left blank, and mention any README items noted above. Don't commit or push unless asked.
