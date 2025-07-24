# My build of st - a simple terminal

This is my custom build of [st](https://st.suckless.org/), a simple terminal originally from the official [suckless](https://suckless.org/) website, customized to suit my personal needs and provide a minimal terminal with all necessary functionality.

## Applied Patches

I have applied the following patches to enhance functionality and appearance:

- [`alpha`](https://st.suckless.org/patches/alpha/)
- [`boxdraw`](https://st.suckless.org/patches/boxdraw/)
- [`blinking_cursor`](https://st.suckless.org/patches/blinking_cursor/)
- [`clickurl`](https://st.suckless.org/patches/clickurl-nocontrol/)
- [`expected-anysize`](https://st.suckless.org/patches/anysize/)
- [`glyph_wide_support`](https://st.suckless.org/patches/glyph_wide_support/)
- [`glyph_wide_support_redraw_fix`](https://github.com/LukeSmithxyz/st/pull/349)
- [`scrollback_mouse`](https://st.suckless.org/patches/scrollback/)
- [`scrollback_ringbuffer`](https://st.suckless.org/patches/scrollback/)
- [`swapmouse`](https://st.suckless.org/patches/swapmouse/)

## Patch Functionality

These patches enhance the usability and appearance of **st** by adding support for transparency, a blinking cursor, wide glyphs (including emojis and Nerd Fonts), improve rendering of box drawing characters and block glyphs. They also enable smooth mouse-based scrollback, a ring buffer for terminal history, and allow resizing the terminal to any dimensions. Together, they provide a more complete and modern terminal experience while keeping **st** lightweight and minimal.

The `clickurl` patch highlights URLs by underlining them and coloring them blue, supports multiple URLs per line, and correctly excludes trailing punctuation; URLs spanning multiple lines are not supported. Left-clicking a URL opens it in the default browser. The `swapmouse` patch changes the mouse cursor to the global default when a running program enables mouse mode.

## Additional Customizations

- Installed **CaskaydiaCove Nerd Font** at 18px size
- Included the [Starship](https://starship.rs/) cross-shell promt
- Changed colors to [Catppuccin Mocha](https://github.com/catppuccin/catppuccin) colorscheme using this [style guide](https://github.com/catppuccin/catppuccin/blob/main/docs/style-guide.md)
- Alpha patch enables transparency (needs a composite manager running)
- I use `xcompmgr` on lightweight systems, and `picom` on more capable ones
- Added 5px border padding around the terminal window

## Key Bindings

This build of **st** uses the default key bindings.  
Clipboard-related shortcuts like `Alt + C` and `Alt + V` are configured in my `dwm` setup and call `cliphist` via `dmenu`.  
You can find the clipboard history script here: [cliphist](https://github.com/sebastianzehner/cliphist)

## Installation

```bash
git clone https://github.com/sebastianzehner/st
cd st
sudo make install
```

## Disclaimer

I'm not a professional developer - just a hobbyist sharing my personal setup.  
This build is provided as-is, with no guarantees that it will work for you.  
If something breaks, you're on your own — but feel free to explore, adapt, and improve!
