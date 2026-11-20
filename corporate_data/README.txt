Corporate mapping data for step 3 of Project UAT.ipynb

legal_names.csv          Hand-checked: the registered company behind a brand name in the BOM, with source.
documented_parents.csv   Hand-checked: parent companies stated in company filings or news, with source and the words relied on.
gleif/                   Saved answers from the GLEIF API (api.gleif.org), pulled 11 November 2026.
                         search_<name>.json = name search; <LEI>_direct-parent.json, <LEI>_ultimate-parent.json = parent records;
                         <LEI>_no-parent-reason.json = the reason a company reports no parent.
wikidata/                Saved answers from the Wikidata API (wikidata.org), pulled 11 November 2026.
                         search_<name>.json = name search; <Q number>.json = one Wikidata record.

The notebook reads these files and only fetches what is missing, and only when PULL = True in section 3.1.
opencorporates/          Saved answers from the OpenCorporates API (api.opencorporates.com), pulled 19 November 2026.
                         search_<name>_<country>.json = name search among the companies registered in that country.
                         worldwide_check_2026-11-19.csv = a second search without the country limit, kept as a record;
                         the same-name companies it found abroad are not used.
                         Company data from OpenCorporates (opencorporates.com), used under its open-data terms.
