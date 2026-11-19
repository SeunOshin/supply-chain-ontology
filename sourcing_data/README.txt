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
