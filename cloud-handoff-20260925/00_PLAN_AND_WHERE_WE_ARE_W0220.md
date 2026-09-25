# EYES CHECK OF EVERY CARD ON THE V10F PAGES - PLAN AND WHERE WE ARE (window 0220, Opus 5.5 ultracode, 2026-09-24 ~22:40 local)

## TOM'S ORDER (his words, this window)
"find a way to read these fucking things on your own without me fucking pasting" / "look at the whole fucking HTML... so that you can see that the words on
the left don't match the words on the right. Or... the number in the box clearly is not the number in the item" / "I'm not pasting shit with upside down
sideways pictures" / "you start this on a new window or save as you go. Don't lose all our data" / "this is not guesswork... that's idiot work [= Claude's job]".
He said the check is Claude's job, and it must be known, not guessed. He will paste ONCE, when everything is right.

## FOUND BEFORE THE CHECK (measured)
- The V10F cards copy the live cards, and the live cards still link the 904 SIDEWAYS photos (275 cards, 51 of 59 pages, 79 as the big top photo).
  The upright copies WERE pushed 09-18 to GitHub folder upright-20260918/ (one tested: HTTP 200). Map old -> new:
  C:\CARD BUILD PLAN - SAMPLE A - 20260916\PHOTO_FIX_STAGED_20260918\01_SIDEWAYS_PHOTOS_USED_ON_CARDS_OLD_TO_NEW_20260918.csv (904 rows).
  Tom stopped a curl test of all 904 new URLs mid-run - it has NOT been run. Run it (or let the eyes check prove them) before any swap.
- 50 more WIDE photos on the cards are NOT on the 904 list (could be sideways or wide on purpose - the eyes check decides).
- The browser pane cannot open local files. The Read tool DOES show photos the way a browser does (it applies the EXIF turn: a 1200x900 tag-6 file
  showed upright 900x1200). 2,299 site photos are stored wide with EXIF tag 6 - they display upright; do not flag them by shape.
- Card 3 test by eye: photo sideways (on the 904 list), blocks 0-0-3 = item 3, typed words include a clean second version (shot 14) that is on no photo of this card.

## THE CHECK
Inputs (one per page): 02_INPUT_ONE_FILE_PER_PAGE\*.json - per card: number, name, type, summary, typed words, photos with the exact local file that
shows what the site shows (mirror file; the 394 rotated-over ones from C:\TOM DECK V15 - PHOTO FIX - 20260915\rotated-photos\; for the 904 sideways
ones the UPRIGHT copy, so the reader proves the replacement is upright).
Batches: 02_CHUNKS_ALL_W0220.csv - 210 batches of up to 10 cards / 30 photos. G01 8, G02 5, G03 42, G04 5, G05 57, G07 18, G08 2, G09 3, G10 1, G11 69.
Per card the reader returns: number blocks seen + verdict, way up per photo, words verdict, name verdict, other problems, how sure.
Results: 03_RESULTS_READER_A\<page>__cards_<from>-<to>__READER_A.json, one file per batch, written when the batch finishes.
Reader B (second independent reader, Tom's photo rule) goes in 04_RESULTS_READER_B\ after reader A has covered everything - first on every card
reader A flagged, then a share of the clean ones.

## RUNS (2 agents at a time on this PC; ~20-minute bursts; Opus 5.5 only)
Burst 1: G01 songs, 8 batches, 74 cards - workflow run wf_869d15a9-18c (launched ~22:40).
Next bursts: G02 + G04 (10 batches), then G03 in 3 bursts, G05 in 4, G07-G10, G11 in 4. Resume = skip every batch whose results file exists.

## AFTER THE CHECK
Every fault type becomes a rule over all 1,644 (new V10G files, nothing old touched): swap sideways photos to their upright copies, fix names,
flag or fix wrong words / wrong numbers. Anything that needs a new photo upload to GitHub waits for Tom's yes. Then one build, one check, one paste.

## USAGE
Weekly all models 91% at the start of window 0220 (resets Sat 26 Sep ~01:00 local). If it runs out mid-check, everything already saved stays.
