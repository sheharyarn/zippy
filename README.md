Zippy
=====

> Zippy is a Ruby Program that allows you to download files from Zippyshare.com in your terminal


## Installation

### OSX

On OSX, you can install it using [`Homebrew`](http://brew.sh):

```bash
$ brew tap sheharyarn/tap
$ brew install zippy
```

### Others (Manual Installation)

First, clone the repo on your system, and then move the script to your `bin` directory:

```bash
$ git clone https://github.com/sheharyarn/zippy
$ chmod +x zippy/zippy
$ mv zippy/zippy /usr/local/bin/
$ rm -rf zippy
```

Make sure the [Dependencies](https://github.com/sheharyarn/zippy#dependencies) are in order as well.

## Usage

```bash
$ zippy link1 link2 link3...

# Example:
$ zippy http://www49.zippyshare.com/v/Ytnd6gVS/file.html
```

## Dependencies

`zippy` depends on the following programs. It needs them to work, so when installing manually, make sure
they are installed as well. No need to do anything when installing from `Homebrew`.

 - [Ruby](https://www.ruby-lang.org/)
 - [wget](https://www.gnu.org/software/wget/)


## TODO

 - Add `--verbose` feature
 - Add `--quiet` feature
 - Add `--continue` feature


## Contributing

1. [Fork it](https://github.com/sheharyarn/zippy/fork)
2. Create your feature/fix branch (`git checkout -b feature/my-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin feature/my-feature`)
5. Create a new Pull Request


## License

Copyright (c) 2015 Sheharyar Naseer

MIT License

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


