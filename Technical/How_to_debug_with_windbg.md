#How to debug with windbg
windbg is a powerful tool which can not only parse process dump but also to debug binary with source code. The following is detail steps and config.

0. Download gflag and windbg from microsoft.

1. Set gflag for binary "XXX.exe" with flag "create user mode stack trace database" and "stack trace" (setting to 50 mb).
(./gflag_setting.png)

2. Set "symbol search path" and "source search path" as the following. The "symbol search path" saves the pdb files for the binary, it can be local path or http link.
(./search_path1.png)
(./search_path2.png)
(./search_path3.png)

3. Start the binary, and attach the windbg to it. Run the following commands.
XXX> .reload

4. Set the break point as the following, and then press "Go". The binary will stop at the break point, the rest thing will be like debugging in VS.
XXX> bp SomeClass::SomeMethods
