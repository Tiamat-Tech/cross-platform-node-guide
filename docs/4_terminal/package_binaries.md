# 💻 Package binaries

Package binaries
([`package.json`'s `bin` field](https://docs.npmjs.com/files/package.json#bin))
are installed in the `node_modules/.bin` directory by `npm install`.

On Unix those are symlinks pointing to the executable files. They can be
executed directly inside a terminal.

On Windows, each package binary
[creates instead three files](https://github.com/npm/cmd-shim) for the same
purpose:

- a Windows batch file ending with `.cmd` executed when using `cmd.exe`.
- a Bash file with no file extension executed when using Cygwin or MSYS2.
- a Powershell file ending with `.ps1` executed when using Powershell.

To fire local binaries on any OS: use [`npx`](https://github.com/zkat/npx) (in
the shell) or [`execa`](https://github.com/sindresorhus/execa) (in JavaScript).

<hr>

[**Next** _(💻 Environment variables)_](environment_variables.md)\
[**Previous** _(💻 File execution)_](file_execution.md)\
[**Top**](README.md)
