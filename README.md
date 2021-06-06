# nvim-parinfer (WIP)

**NOTE:** I have noticed some strage bugs (in indent and smart mode at least),
and currently I do not have the time to hunt them down - the problem may be in
the Lua library itself - , so consider this as WIP for the moment (or use it at
your own risk).

Fast and light [parinfer](https://shaunlebron.github.io/parinfer/) plugin for
Neovim.

### Why?

The two maintained parinfer plugins currently available for (Neo)Vim both have
certain drawbacks: The good old [VimL
plugin](https://github.com/bhurlow/vim-parinfer) uses the library ported by
[oakmac](https://github.com/oakmac/), which implements an older version of
Parinfer, and - unfortunately - is terribly slow, often on the verge of being
unusable. The more recent [Rust
port](https://github.com/eraserhd/parinfer-rust), on the other hand, while
super-fast and very polished, requires building dynamic libraries and a Rust
toolchain for that, which makes it inconvenient for less involved users, not to
say that it takes up a considerable amount of disk space too. (If you're fine
with these, just go ahead and use it of course!)

With a [Lua library](https://github.com/oakmac/parinfer-lua) available (thanks
to Chris Oakman, again!), we can have the best of both worlds now, a lightweight
yet fast plugin in the native scripting language of the editor, with hassle-free
installation and the latest features (smart mode) provided.

All credit goes to the aforementioned authors, I just took the Vim plugin and
the doc file from the parinfer-rust repo, and made trivial modifications to
stitch it together with the Lua lib. 

## Install

Use your favourite package manager, e.g.
[vim-plug](https://github.com/junegunn/vim-plug):

```
Plug 'ggandor/nvim-parinfer'
```

