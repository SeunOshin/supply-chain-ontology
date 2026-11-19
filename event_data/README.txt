Event data for step 5 of Project UAT.ipynb

event_sources.csv   The sources. Six "library" rows are the pages chosen by hand for the five events in the typed event library.
                    251 "news feed" rows are the headlines of the news collection saved on 10 November 2026 (window 7 to 9 November 2026).
news_screen.csv     Claude's screening of the 251 headlines: relevant yes or no, with a short reason. 15 were marked relevant.
event_library.csv   One row per source that went through extraction (the 6 library pages and the 15 relevant headlines).
                    Claude filled in the event fields from the page and gave a decision (claude_decision, claude_reason).
                    "decision" is the one the notebook uses. It starts as Claude's. To overrule it, change it to accepted or rejected
                    and put your name in decided_by. Rows with the same event_key are one event with several sources.

Screening and extraction were run on 12 November 2026 with claude-sonnet-5-5. Page text is not saved, only the result and the link.
The notebook reads these files. It only asks Claude again when PULL = True and a source has no saved answer.
