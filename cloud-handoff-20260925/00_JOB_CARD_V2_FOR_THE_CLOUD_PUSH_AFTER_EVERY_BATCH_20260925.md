# JOB CARD V2 FOR A CLAUDE CLOUD SESSION - READ THIS FIRST, THEN V1 - written 2026-09-25 02:30, window 0223

V1 (00_JOB_CARD_FOR_THE_CLOUD_20260925.md, in this same folder) has the whole job: who Tom is, the rules,
where the photos are, what to check, how to resume. READ IT. Everything in it still stands.
V1 left out three things. They are below. They are not optional.

## 1. COMMIT AND PUSH AFTER EVERY BATCH. YOUR DISK IS TEMPORARY.

This machine is wiped when the session goes idle. Anything only on this disk is gone when that happens.
So the rule from Tom's CLAUDE.md - SAVE AS YOU GO - means, here, PUSH AS YOU GO:

    after EVERY batch of ~10 cards:
        git add cloud-handoff-20260925/04_RESULTS_READER_A_CLOUD/<the new file>
        git commit -m "Cloud reader A: <page> cards <from>-<to>"
        git push

Push to whatever branch you are on. A branch is fine. A pull request is fine. What is NOT fine is a
result that exists only on this machine. If a push fails, stop and say so - do not keep reading cards
whose results cannot be saved.

Also keep a running CSV, one row per card, in the same folder, and push it with every batch:
    04_RESULTS_READER_A_CLOUD/00_ALL_RESULTS_SO_FAR_CLOUD.csv
Same columns as 07_READER_A_RESULTS_WINDOW_0220_CLOSE_20260924_2327_549_CARDS.csv so the two sets merge.

## 2. BEFORE THE 1,095: PROVE YOU CAN SEE THE PHOTOS. THREE CARDS ONLY.

Pick the first batch of G05 (02_CHUNKS_ALL_W0220.csv). Do THREE cards, not ten. For each, open every one
of its photos from this repo (the REPO_PATH column in 01_EVERY_PHOTO_..._W0220.csv; the file is in this
checkout, no web fetch needed) and write down, in plain words:
  - what number the small number card in the photo reads (digits stacked, read bottom to top)
  - the first line of handwriting you can read on the sheet
  - whether the photo is upright, sideways or upside down
Push that as 04_RESULTS_READER_A_CLOUD/00_THREE_CARD_EYES_TEST.md and then STOP and tell Tom what you saw.

If you cannot actually see the images - if you are describing file names or guessing from the typed
words - SAY SO and stop. Do not run the 1,095. Tom would rather have nothing than 1,095 guesses.

## 3. NEVER ASK TOM TO DECIDE A CARD'S FATE. THE ANSWER IS ALREADY WRITTEN.

If you find yourself about to ask "should I skip / merge / drop / hide this card?" - the answer is NO,
from CLAUDE.md, every time. Report it and move on. A card with no photo, a card whose number is wrong,
a card that looks like another card: all real, all stay, all get a row in the results.

Do not touch the website. Do not overwrite any existing file. New files, new names, only.
