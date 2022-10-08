## Table Scan
- Database divided into -> Extents (64Kb) -> Data Pages (8Kb) -> Rows (1Kb).
- Each Data Page can have maximum of 8 Rows.
- Table Scan will search each row sequentially to find row which satisfies WHERE condition.

## Index Seek
- Indexes divided into -> Index Pages (8Kb). 
- Each page has the id of each Row(Integer - 4 bytes), so Each Page can have a maximum of 2000 Rows.
- So we need to search in which range our column lies in each node of BTree without actually seacrhing across each row.
- BTree inorder traversal gives rows in sorted order.
- Each Index id saves Extent number, Page number and row offset.

## For 8 Terrabyte data, in Table scan, pages searched = 47 and in Index Seek , pages searched = 3.
