Trade and tariff data for step 4 of Project UAT.ipynb

fairphone4_tariff_codes.csv   Review file. One row per good: the HS code, the EU code, and a decision on each
                              (accepted, proposed or unclassified) with the reason. Ten HS codes were accepted in October 2026;
                              the EU codes and twelve further HS codes were proposed and accepted on 11 November 2026. Seven broad supplier categories are left unclassified.
                              To accept a proposal, change its decision to "accepted" and run step 4 again.
skydio_x10_tariff_codes.csv   Review file for Skydio. All codes were reviewed and accepted on 10 November 2026 (US HTS 2026 Revision 22).
skydio_x10_us_duties.csv      US duty measures for the Skydio codes, one row per duty. Reshaped on 11 November 2026 from the US tariff
                              lookups saved on 10 November 2026 (the duty stack, the supply-line duties and the rate changes).
eu/                           Saved answers from the UK tariff service's Northern Ireland feed, which carries the EU tariff
                              (trade-tariff.service.gov.uk/xi), one file per code, pulled 11 November 2026.
uk/                           The same codes from the UK feed, used only if the EU feed has no answer.
eu_headings/                  Heading listings used to find the declarable EU lines under each HS code.

The notebook reads these files and only fetches a missing code when PULL = True in section 3.1.
