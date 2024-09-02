# My build of st

My personal build of st

## About
I use this repository as a way to version control any changes I make to my terminal emulator. My terminal emulator contains keybindings and other customizations that are adopted to my own workflow, and thus, aren't usable for everyone.

## Patches done to st
This build of st is based on [st 0.9.2](https://dl.suckless.org/st/st-0.9.2.tar.gz) (2024-04-05) and is modified with patches and other changes to the source code outside of patches itself. I have kept all used *.diff files* in [master/patches](https://github.com/consoom/st/tree/master/patches):

- [alpha](https://github.com/consoom/st/blob/main/patches/st-alpha-20220206-0.8.5.diff) ([source](https://st.suckless.org/patches/alpha/)) — adds transparency to the background (compositor required)
- [alpha dynamic](https://github.com/consoom/st/blob/main/patches/st-alpha-dynamic-73a6020865607018f6442317e7f94fb5d54a7016.diff) ([source](https://github.com/LukeSmithxyz/st/commit/73a6020865607018f6442317e7f94fb5d54a7016)) — allows you to change the alpha variable via shortcuts
- [alpha focus offset #1](https://github.com/consoom/st/blob/main/patches/st-focus-69925ee23b8b1590f65e1f71f2d9ea5156629868.diff) and [#2](https://github.com/consoom/st/blob/main/patches/st-alpha-focus-offset-bb56685063532f732f4fbdba1d890931dad3d891.diff) ([source #1](https://github.com/LukeSmithxyz/st/commit/69925ee23b8b1590f65e1f71f2d9ea5156629868) and [#2](https://github.com/LukeSmithxyz/st/commit/bb56685063532f732f4fbdba1d890931dad3d891)) — allows a difference in alpha between focused and unfocused st windows
- [anysize](https://github.com/consoom/st/blob/main/patches/st-anysize-20220718-baa9357.diff) ([source](https://st.suckless.org/patches/anysize/)) — makes st resizable to any size
- [boxdraw](https://github.com/consoom/st/blob/main/patches/st-boxdraw_v2-0.8.5.diff) ([source](https://st.suckless.org/patches/boxdraw/)) — makes graphic lines and blocks align better
- [clickurl](https://github.com/consoom/st/blob/main/patches/st-clickurl-0.8.5.diff) ([source](https://st.suckless.org/patches/clickurl/)) — highlight URLs on screen by holding left control
- [glyph wide support](st-glyph-wide-support-boxdraw-20220411-ef05519.diff) ([source](https://st.suckless.org/patches/glyph_wide_support/)) — fixes wide glyphs truncation
- [scrollback](https://github.com/consoom/st/blob/main/patches/st-scrollback-ringbuffer-0.9.2.diff) — efficient scrolling through output
- [xresources w/ signal reloading](https://github.com/consoom/st/blob/main/patches/st-xresources-signal-reloading-20220407-ef05519.diff) ([source](https://st.suckless.org/patches/xresources-with-reload-signal/)) — change terminal resources like colors and fonts on the fly, reads from Xresources

## Installation & usage
This program is supposed to be used in tandem with my [dotfiles](https://github.com/consoom/comfydots), as it relies on some other software, environment variables, configurations and the like. Although my dotfiles repository includes a bootstrapping script, I don't recommend using my personal configurations without first changing them to your own needs.

### Keybindings

#### Most used keybindings
| **Modifier**            | **Key**   | **Action**                                        |
|-------------------------|-----------|---------------------------------------------------|
|        (Control)        | Scroll up | Scrolls up (control: scrolls up 5 lines)          |
|        (Control)        |Scroll down| Scrolls down (control: scrolls down 5 lines)      |
|       Shift + Alt       | k/↑/pg up | Increment fontsize with 1                         |
|       Shift + Alt       | j/↓/pg dn | Decrement fontsize with 1                         |
|       Shift + Alt       |     u     | Increment fontsize faster                         |
|       Shift + Alt       |     d     | Decrement fontsize faster                         |
|       Shift + Alt       | r / home  | Reset fontsize                                    |
|      (Shift) + Alt      |     c     | Copy terminal text to clipboard                   |
|      (Shift) + Alt      |     v     | Paste clipboard text to terminal                  |
|           Alt           |     k     | Scroll up 1 line                                  |
|           Alt           |     j     | Scroll down 1 line                                |
|           Alt           |     u     | Scroll up faster                                  |
|           Alt           |     d     | Scroll down faster                                |
|           Alt           |     a     | Increment background transparency by 5%           |
|           Alt           |     s     | Decrement background transparency by 5%           |
|         Control         | (mouse 1) | Highlight URLs (click highlighted URL to open)    |
