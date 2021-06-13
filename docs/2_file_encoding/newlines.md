# 📝 Newlines

The character representation of a
[newline](https://en.wikipedia.org/wiki/Newline) is OS-specific. On Unix it is
`\n` (line feed) while on Windows it is `\r\n` (carriage return followed by line
feed).

Newlines inside a template string translate to `\n` on any OS.

<!-- eslint-disable import/unambiguous -->

```js
const string = `this is
an example`
```

Some Windows applications, including `cmd.exe`, print `\n` as newlines, so using
`\n` will work just fine. However some Windows applications don't, which is why
when reading from or writing to a file the OS-specific newline
[`os.EOL`](https://nodejs.org/api/os.html#os_os_eol) should be used instead of
`\n`.

<hr>

[**Next** _(📝 EOF and BOM)_](eof_bom.md)\
[**Previous** _(📝 Character encoding)_](character_encoding.md)\
[**Top**](README.md)
