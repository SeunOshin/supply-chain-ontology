Corporate mapping data for step 3 of Project UAT.ipynb

legal_names.csv          Hand-checked: the registered company behind a brand name in the BOM, with source.
documented_parents.csv   Hand-checked: parent companies stated in company filings or news, with source and the words relied on.
gleif/                   Saved answers from the GLEIF API (api.gleif.org), pulled 11 November 2026.
                         search_<name>.json = name search; <LEI>_direct-parent.json, <LEI>_ultimate-parent.json = parent records;
                         <LEI>_no-parent-reason.json = the reason a company reports no parent.
wikidata/                Saved answers from the Wikidata API (wikidata.org), pulled 11 November 2026.
                         search_<name>.json = name search; <Q number>.json = one Wikidata record.

The notebook reads these files and only fetches what is missing, and only when PULL = True in section 3.1.
OpenCorporates is not used: no API access was granted.
