## Points to remember

* DO NOT CHANGE https://github.com/Cyfrin/up/blob/main/cyfrinup
* DO NOT CHANGE https://github.com/Cyfrin/up/blob/main/install

These files were previsouly downloaded into the existing cyfrinup users' computers. Changing these would **NOT** result in changing those files. Treat these as immutable.

Refer https://github.com/Cyfrin/aderyn/tree/master/cyfrinup to understand how we redirect the old dynamic script to this new dynamic script.

## Make changes   

Only script where changes are allowed (and will make sense) is in the `dynamic_script` located here - https://github.com/Cyfrin/up/blob/main/dynamic_script

* [ ] Call `install_package "tool-name"` in the `main()` function following the current pattern. i.e
    * [ ] Inside the if statement guarded by `CYFRINUP_ONLY_INSTALL`
    * [ ] Inside the else branch

* [ ] In the `install_package()` function, describe the steps you'd take to install the new tool.

* [ ] Update the Readme toolbox

No other kind of change is allowed.

## Misc. Info

- Older Aderyn VS Code extensions set `CYFRINUP_ONLY_INSTALL=aderyn`. Preserve this value as an explicit retirement error so these callers never install another tool as a fallback.
- `CYFRINUP_ONLY_INSTALL=safe-hash` continues to install Safe-Hash. The default invocation warns that Aderyn is retired and installs Safe-Hash only.
