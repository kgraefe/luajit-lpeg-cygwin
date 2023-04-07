# luajit-lpeg-cygwin

This a recipe to build and package [LPeg][1] for [Cygwin][2]. The recipe is
based on the [recipe in cascent's old neovim port][3].

Dependencies:
- [luajit{,-devel}][4]

To build the package install the dependencies and run the following command:
```sh
cygport luajit-lpeg-cygwin.cygport download prepare compile install package
```

To install the package you can extract it into the root directory:
```sh
eval "$(cygport luajit-lpeg.cygport vars PVR)"
tar -C / -xjvf luajit-$PVR.x86_64/dist/luajit-lpeg/luajit-lpeg-$PVR.tar.xz
```

[1]: http://www.inf.puc-rio.br/~roberto/lpeg/
[2]: http://www.cygwin.com/
[3]: https://github.com/cascent/neovim-cygwin/blob/09277e3f76981189a2f15d1dbc2f5a4ab4b6c86f/luajit-lpeg/luajit-lpeg.cygport
[4]: https://github.com/kgraefe/luajit-cygwin
