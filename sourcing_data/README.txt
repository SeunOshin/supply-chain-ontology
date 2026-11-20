Sourcing advice (step 8 of Project UAT.ipynb)

advice.csv    One row for each purchasing instruction, for every BOM item with at least one risk rule
              that returns yes (a High or Moderate finding). Written by Claude from the evidence the
              graph holds for the item, then checked: an instruction may only cite records that are
              in that evidence.

Columns
  case, item_id, item, number    which item, and whether it is its first or second instruction
  strategy                       one of the seven strategies listed in section 8.1
  firmness                       set by the notebook from the suppliers named, not by Claude
  instruction, why               in words; supplier names come from the evidence
  suppliers                      the suppliers to buy from or approach
  addresses                      the risk rules the instruction deals with
  evidence                       other records it rests on
  before_acting                  what must be in place first, separated by " | "
  check                          "passed", or what the reference check found wrong
  decision, decided_by           accepted or rejected. To overrule, change decision here and
                                 run step 8 again. Only accepted instructions enter the graph.
  in_plain_words                 the instruction rewritten by Claude for a business reader. It may only
                                 name suppliers the instruction already names. Shown on the Smart
                                 Procurement tab of the graph preview, after one fixed sentence that
                                 says what the strategy means.

Advice saved here is reused. An item with no row is put to Claude only when PULL is True.

blue_uas_framework.csv   The Blue UAS Framework list of vetted drone parts (226 components), as read on 14 November 2026
                         from flightbrief.news/topics/blue-uas, which gives the official list at bluelist.dcma.mil as
                         its source. Not checked against the official page.
blue_uas_matches.csv     Hand-checked: for a BOM item, the makers on that list of the same kind of part (close) or of a
                         related part only (loose), with the listed components and the reason. Used in section 8.2.

The advice was asked again on 19 November 2026, after the second round of bills and the vetted makers were added.
