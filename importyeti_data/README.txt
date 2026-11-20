ImportYeti data pulled on 11 November 2026 (US customs ocean bills of lading, via the paid ImportYeti API).

company_search/          Free name searches for 44 drone companies: listing, shipment count, top suppliers.
drone_sample/            Counts for the goods search "drone", and a 50-bill sample (10 bills at each of 5 offsets, since 01/01/2023).
part_counts_unfiltered/  Number of bills since 01/01/2023 for 16 BOM part searches, before any filter.
bills_by_part/           Bills bought by the Project UAT notebook, one folder per part (house bills between different companies).
                         First round, 11 November 2026: up to 300 bills per part (3,352 bills).
                         Second round, 19 November 2026: the cap raised for eight parts, and a second, wider search for
                         seven parts whose first search ran out, saved in <part>_wider (5,160 more bills; 8,492 in all).
                         part_counts.json and wider_counts.json hold the number of bills available for each search.

Raw API replies are kept as returned. They include company addresses and phone numbers.
