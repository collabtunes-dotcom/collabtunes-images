# JOB CARD FOR A CLAUDE CLOUD SESSION - THE EYES CHECK - written 2026-09-25, window 0223

Read this whole file before doing anything. You are a cloud session. You have NO access to Tom's C: drive.
Everything you need is in this folder / repo. The photos come from GitHub.

## WHO AND WHAT

Tom Jensen owns COLLABTUNES.COM. He is selling ~2,000 original handwritten lyric and poem sheets.
Each sheet is a CARD on a web page. The job is to CHECK EVERY CARD with eyes on the photos before he
pastes anything to the website. He has pasted twice already and will not paste again until every card is right.

His words: "look at the whole HTML - the words on the left don't match the words on the right - the number
in the box is not the number in the item" / "I'm not pasting shit with upside down sideways pictures" /
"this is not guesswork" / "save as you go. Don't lose all our data."

## THE RULES YOU MAY NOT BREAK

1. EVERY NUMBER IS ITS OWN ITEM. Two cards with the same title are two different sheets of paper.
   There are NO duplicates, doubles, twins or copies in this catalogue. Never use those words about it.
2. NEVER hide, fold, merge or remove a card - not for looking like another card, not for having no photo.
   A card with no photo is a real item whose photo has not been found yet. Every run must lose 0 cards.
3. ONE PHOTO = ONE NUMBER: the number its own blocks read. Digits are stacked vertically on a small card
   inside the photo, read BOTTOM TO TOP, zero-padded. If a photo's blocks read a different number than the
   card it sits on, that is a DATA ERROR: report it. The photo belongs to the number in its blocks.
4. ADD ONLY. Never overwrite or delete an existing file. New findings go in NEW files with NEW names.
5. SAVE AS YOU GO. Write one results file per batch the moment the batch finishes. Never hold results in
   memory to write at the end. A crash must cost one batch, never the run.
6. THIS IS NOT GUESSWORK. If you cannot see it, say you cannot see it. Never invent a number or a word.

## WHERE THE PHOTOS ARE - THIS IS THE CLOUD SWAP

On Tom's PC the reader opened photos as local files. You cannot. Instead:

    https://raw.githubusercontent.com/collabtunes-dotcom/collabtunes-images/main/<REPO_PATH>

REPO_PATH is a column in 01_EVERY_PHOTO_ON_V10F_WITH_LOCAL_FILE_AS_SITE_SHOWS_W0220.csv.
URL-encode spaces and parentheses. Ignore the LOCAL_AS_SITE_SHOWS and UPRIGHT_COPY columns - those are
C: drive paths and mean nothing to you.

OPEN QUESTION, DO NOT GUESS: some photos have an "upright" corrected copy that may or may not be in the
repo under a different name. If a photo looks sideways or upside down, REPORT IT as WAY_UP. Do not try to
find or make a corrected copy. That is Tom's call, and a new upload needs his yes.

## THE FILES IN THIS FOLDER

- 02_INPUT_ONE_FILE_PER_PAGE\        59 json, one per page. Each holds its cards: item_number,
                                     name_on_card, item_type, summary, typed_words, and the photo list.
- 02_CHUNKS_ALL_W0220.csv            210 batches. Each row is one batch of ~10 cards to check.
- 01_EVERY_PHOTO_..._W0220.csv       every photo on every card -> its REPO_PATH (the GitHub link).
- 03_RESULTS_ALREADY_DONE_READER_A\  60 batch json ALREADY DONE. 549 cards. DO NOT REDO THESE.
- 07_READER_A_RESULTS_..._549_CARDS.csv   the same 549 cards, one row each.
- 06_WORKFLOW_SCRIPT_READER_A_W0220.js.txt  the script the PC used. Reference for the output shape.
- START_HERE_ITEM_TYPES_..._V11_...md      the full state of the project as of 2026-09-24.
- 00_PLAN_AND_WHERE_WE_ARE_W0220.md        the method, written by the window that built it.

## HOW TO RESUME - THE 1,095 CARDS LEFT

Take every row of 02_CHUNKS_ALL_W0220.csv whose results file
    <page>__cards_<from 2 digits>-<to 2 digits>__READER_A.json
is NOT already in 03_RESULTS_ALREADY_DONE_READER_A\. That is 150 batches, 1,095 cards.

LEFT BY GROUP: G05 (57 batches, 557 cards), G07 (18, 111), G08 (2, 16), G09 (3, 23), G10 (1, 3),
G11 (69 batches, 385 cards, 1,500 photos).

Write each finished batch to a NEW folder, 04_RESULTS_READER_A_CLOUD\, same file naming. Never write into
03_. After every batch also append to a running CSV so a crash keeps everything already read.

## WHAT TO CHECK ON EACH CARD

For each card, look at every one of its photos and answer:

- NUMBER      - do the photo's blocks read this card's item_number? If not, what number do they read?
- NAME        - is the name written on the sheet? Does it match name_on_card? If the sheet shows a
                different or better name, put it in NAME_NOTE.
- WORDS       - do the typed_words match the words on the sheets? Flag: small differences, typed words
                that include a sheet not pictured, sheet words not typed, words that came off another sheet.
- WAY_UP      - is the photo upright as a person would hold the sheet? Sideways / upside down = flag.
                A wide overview shot that is meant to be landscape is NOT a fault.
- READABLE    - blurry, cut off, too dark to read.

Every flag names the photo it came from. Never a flag without a photo behind it.

## WHAT THE FIRST 549 ALREADY SHOWED - so you know what you are looking for

221 of 549 (40%) had at least one real problem.
- NUMBER, 20 cards. THE SHIFT: Tom doubled number 23 (Old Eyes and Blank Pages are both 23) and the
  numbers after it slid by one - cards 24-30 each show the number before them. He thinks 50-100 cards
  are affected. Watch for it everywhere. Other known ones: 175 reads 174, 183 reads 1583 (a CD),
  1100 reads 375 on all three photos, 238 has 240's pages, 501 has 502's, 523 has 255's, 956 has 952's,
  1629 has 1630's, 1731 has 1732's, 1763 has 1764's, 1764 has 1765's (a guitar), 1986 has 1982's.
- WAY_UP, 19 cards / 36 photos, even after an earlier upright pass. Judge every photo on its own.
- NAMES, 62 cards with no name on the sheet or junk in the name.
- WORDS: 292 matched, 86 small differences, 104 typed a sheet that is not pictured, 57 sheet words not
  typed, 10 had words off another sheet.

## WHAT HAPPENS AFTER YOU

You do NOT fix anything and you do NOT touch the website. Nobody does - Tom pastes, by hand, once, at the
end. Your job ends at the findings files. A window on Tom's PC pulls them down, turns each fault type into
a rule across all 1,644 cards, rebuilds the pages as NEW files, and hands Tom one paste.

## OPEN QUESTIONS - REPORT, DO NOT DECIDE

1. 1,644 cards on the pages vs 1,584 rows in CARDS_ALL_1584_FOR_CLOUD_20260925.csv. The 60 difference is
   not explained. Do not drop a card over it. Flag it.
2. The upright copies (above).
3. 349 "unreleased" poems in books were never split out. Not your job, but do not let it confuse a count.
