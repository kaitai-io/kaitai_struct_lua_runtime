# Kaitai Struct: runtime library for Lua

This library implements Kaitai Struct API for Lua 5.3 and 5.4.

Kaitai Struct is a declarative language used for describe various binary
data structures, laid out in files or in memory: i.e. binary file
formats, network stream packet formats, etc.

Further reading:

* [About Kaitai Struct](http://kaitai.io/)
* [About API implemented in this library](http://doc.kaitai.io/stream_api.html)

## Installation

1. You can clone the runtime library with Git:

   <pre><code>git clone <strong>--recurse-submodules</strong> https://github.com/kaitai-io/kaitai_struct_lua_runtime.git</code></pre>

   If you clone without `--recurse-submodules`, the runtime library will work too, but you'll not be able to parse formats that use `process: zlib` - calling `KaitaiStream.process_zlib` will fail. If you need _zlib_ support but the runtime was cloned without `--recurse-submodules`, run:

   ```bash
   git submodule update --init --recursive
   ```

2. Or if you want to add the runtime library to your project as a Git submodule:

   ```bash
   git submodule add https://github.com/kaitai-io/kaitai_struct_lua_runtime.git [<path>]
   git submodule update --init --recursive
   ```

   The second command is only required if you need support for `process: zlib`.

## Licensing

Copyright 2017-2025 Kaitai Project: MIT license

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
