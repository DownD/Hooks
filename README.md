# Hooking Library

This is a simple library used to hook x86 functions in windows systems.
The current available types of hooks are:
- JMP Hook with trampoline
- Mid function JMP Hook with trampoline
- Return Hook with trampoline
- Detours Hook by Microsoft (https://github.com/microsoft/Detours)
- Sleep Hook (Simple jmp hook on the sleep function)

Each hook can be used by creating a `Hook` object and calling `HookFunction` hook the function and `UnHookFunction` to unhook.
Each hook type as it's draw backs, but most of them require a minimum number of bytes to hook and cannot be set over a relative jmp or call instruction.
More details are available on each include header.