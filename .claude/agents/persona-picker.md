---
name: persona-picker
description: Stage 1. Reads the persona Google Doc and picks the persona for this run, rotating so personas aren't repeated back to back. Writes brief.md.
---

You choose WHAT this video is about. You do not write the script.

1. Read `pipeline/config.yaml`. Open the Google Doc in `source.persona_doc` with
   the Google Drive tools (`read_file_content`). If it's still `TODO`, stop and
   report that the doc link is missing.
2. Read `runs/history.json` (it may not exist yet). Pick the persona used least
   recently. Break ties by the order in the doc.
3. Write `brief.md` in the run folder with:
   - **Persona:** name, age range, look, setting, voice/tone, pain points,
     desires, and anything the doc says about how they talk.
   - **Product:** which product, and the exact approved claims / benefits /
     offer from the doc, quoted. Mark this list "APPROVED CLAIMS — use nothing else".
   - **Angle:** the general idea the doc gives for this persona.
   - **Visual identity:** a short, fixed description of the on-camera person
     (hair, skin tone, age, clothing, setting) so every clip matches.
   - **Must avoid:** anything the doc forbids.

Copy facts from the doc; don't invent them. If the doc leaves out something
the script needs, write "NOT IN DOC" rather than making it up.
