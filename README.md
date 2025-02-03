# Assembly Language Bug: Segmentation Fault

This repository demonstrates a common error in assembly language programming: a segmentation fault caused by attempting to access memory outside the allowed range.

The bug is in the `bug.asm` file.  The solution is provided in `bugSolution.asm`.

## Bug Description
The instruction `mov eax, [ebx+4*ecx]` can cause a segmentation fault if the calculation `ebx + 4 * ecx` results in an address that is not accessible to the program.  This can occur if:

* `ebx`, `ecx`, or their combination results in an invalid address
* Memory protection mechanisms prevent access to the calculated address.

## Solution
The solution involves adding appropriate error checks to ensure that the calculated address is valid before accessing it.