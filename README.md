# COBOL Data Truncation Bug

This repository demonstrates a subtle bug in a COBOL program that can lead to unexpected data truncation. The problem arises from an insufficiently defined PIC clause, leading to unpredictable behavior depending on the data length.  The bug is not immediately obvious and may be difficult to diagnose in larger programs.

## Bug Description
The `bug.cob` program moves data from one area to another. If the length of the data exceeds the PIC clause definition of the receiving area, truncation occurs silently, leading to potential errors.  This bug becomes more insidious when the data length isn't consistently long or short.

## Solution
The `bugSolution.cob` program corrects the problem by ensuring that the PIC clauses provide sufficient space to accommodate the data.  This eliminates potential data truncation, leading to reliable program behavior.