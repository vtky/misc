Calling Conventions
===================


System V x64
-------------
Parameters to functions are passed in the registers **rdi, rsi, rdx, rcx, r8, r9** and further values are passed on the stack in reverse order.

Register | Usage
-------- | ---
%rdi | used to pass 1st argument to functions
%rsi | used to pass 2nd argument to functions
%rdx | used to pass 3rd argument to functions; 2nd return register
%rcx | used to pass 4th integer argument to functions
%r8 | used to pass 5th argument to functions
%r9 | used to pass 6th argument to functions
- | -
 %rax | temporary register; with variable arguments passes information about the number of vector registers used; 1st return register
 %xmm0–%xmm1 | used to pass and return floating point arguments
 %xmm2–%xmm7 | used to pass floating point arguments

http://wiki.osdev.org/System_V_ABI

https://www.uclibc.org/docs/psABI-x86_64.pdf

----------

ARM
-------------
Register | Usage
-------- | ---
r0 - r3 | used to hold argument values passed to a subroutine, and also hold results returned from a subroutine.
r4 - r11 | used to hold local variables.
r12 | Intra-Procedure-call scratch register
r13 | stack pointer. (The Push/Pop instructions in "Thumb" operating mode use this register only).
r14 | link register. (The BL instruction, used in a subroutine call, stores the return address in this register).
r15 | Program Counter

http://infocenter.arm.com/help/topic/com.arm.doc.ihi0042f/IHI0042F_aapcs.pdf

----------


ARM64
-------------

Register | Usage
-------- | ---
x0 - x7 | used to hold argument values passed to a subroutine, and also hold results returned from a subroutine.
x8 | used to hold indirect return value address
x9 - x15 | used to hold local variables (caller saved)
x16 - x18 | Intra-Procedure-call scratch register
x19 - x28 | callee-saved
x29 | frame register
x30 | link register (used to return from subroutines)

http://infocenter.arm.com/help/topic/com.arm.doc.ihi0055b/IHI0055B_aapcs64.pdf
