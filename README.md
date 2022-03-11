## [Download latest release](https://github.com/ledoge/i1d3_hook/releases/latest/download/i1d3_hook.dll)

# About
This DLL allows you to use (almost) any branded OEM variant of the i1Display Pro with most (?) Windows software that supports the i1Display Pro colorimeter. It works by hooking some of the functions provided by the official i1D3 SDK to provide the right unlock code and make it look like the generic OEM variant.

# Usage
1. Make sure that the software you want to use the colorimeter with uses the official i1d3 SDK (`i1d3SDK.dll` or `i1d3.dll`), and that the SDK DLL is loaded already.
2. Use any DLL injector, such as [Extreme Injector](https://github.com/master131/ExtremeInjector), to inject `i1d3_hook.dll` into the software.
3. Make the software (re-)scan for devices, and it should see your colorimeter.

# Compiling
Using a 32-bit MinGW build of GCC with the MinHook package installed:

`gcc i1d3_hook.c -Os -shared -static -s -lMinHook -Wl,--exclude-all-symbols -o i1d3_hook.dll`
