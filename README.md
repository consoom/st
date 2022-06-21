# My build of st

My personal build of st

## About
I use this repository as a way to version control any changes I make to my terminal emulator. My terminal emulator contains keybindings and other customizations that are adopted to my own workflow, and thus, aren't usable for everyone. You might however take inspiration out this build or contribute and suggest improvements. A lot of keybindings and general tools in this build rely on other programs and configurations that I keep track of in my [dotfiles repository](https://github.com/consoom/comfydots).

## Patches done to st
This build of st is based on [st 0.8.5](https://dl.suckless.org/st/st-0.8.5.tar.gz) (2022-01-07) and is modified with patches and other changes to the sourcecode. I have kept all used *.diff files* to patch st with in [master/patches](https://github.com/consoom/st/tree/master/patches):

- [alpha](https://github.com/consoom/st/blob/main/patches/st-alpha-20220206-0.8.5.diff) ([source](https://st.suckless.org/patches/alpha/)) — adds transparency to the background (compositor required)
- [alpha dynamic](https://github.com/consoom/st/blob/main/patches/st-alpha-dynamic-73a6020865607018f6442317e7f94fb5d54a7016.diff) ([source](https://github.com/LukeSmithxyz/st/commit/73a6020865607018f6442317e7f94fb5d54a7016)) — allows you to change the alpha variable via shortcuts
- [alpha focus offset #1](https://github.com/consoom/st/blob/main/patches/st-focus-69925ee23b8b1590f65e1f71f2d9ea5156629868.diff) and [#2](https://github.com/consoom/st/blob/main/patches/st-alpha-focus-offset-bb56685063532f732f4fbdba1d890931dad3d891.diff) ([source #1](https://github.com/LukeSmithxyz/st/commit/69925ee23b8b1590f65e1f71f2d9ea5156629868) and [#2](https://github.com/LukeSmithxyz/st/commit/bb56685063532f732f4fbdba1d890931dad3d891)) — allows a difference in alpha between focused and unfocused st windows
- [anysize](https://github.com/consoom/st/blob/main/patches/st-anysize-0.8.4.diff) ([source](https://st.suckless.org/patches/anysize/)) — makes st resizable to any size
- [boxdraw](https://github.com/consoom/st/blob/main/patches/st-boxdraw_v2-0.8.5.diff) ([source](https://st.suckless.org/patches/boxdraw/)) — makes graphic lines and blocks align better
- [scrollback #1](https://github.com/consoom/st/blob/main/patches/st-scrollback-ringbuffer-0.8.5.diff), [#2](https://github.com/consoom/st/blob/main/patches/st-scrollback-mouse-20220127-2c5edf2.diff) and [#3](https://github.com/consoom/st/blob/main/patches/st-scrollback-mouse-altscreen-20220127-2c5edf2.diff) ([source](https://st.suckless.org/patches/scrollback/)) — adds support for scrolling back through the terminal (also with a scroll wheel)
- [xresources w/ signal reloading](https://github.com/consoom/st/blob/main/patches/st-xresources-signal-reloading-20220407-ef05519.diff) ([source](https://st.suckless.org/patches/xresources-with-reload-signal/)) — change terminal resources like colors and fonts on the fly, reads from Xresources

## Installation
I don't recommend using my personal build without changing the configuration, as it's adopted to satisfy my own workflow. It's supposed to be installed and used  together with my [dotfiles](https://github.com/consoom/comfydots). Here are the install instructions:
```
$ git clone https://github.com/consoom/st
$ cd st
$ sudo make clean install
```

## Keybindings

### Most used keybindings
| **Modifier**            | **Key**   | **Action**                                        |
|-------------------------|-----------|---------------------------------------------------|
|        (Control)        | Scroll up | Scrolls up (control: scrolls up 5 lines)          |
|        (Control)        |Scroll down| Scrolls down (control: scrolls down 5 lines)      |
|       Shift + Alt       | k/↑/pg up | Increment fontsize with 1                         |
|       Shift + Alt       | j/↓/pg dn | Decrement fontsize with 1                         |
|       Shift + Alt       | r / home  | Reset fontsize                                    |
|      (Shift) + Alt      |     c     | Copy terminal text to clipboard                   |
|      (Shift) + Alt      |     v     | Paste clipboard text to terminal                  |
|           Alt           |     k     | Scroll up 1 line                                  |
|           Alt           |     j     | Scroll down 1 line                                |
|           Alt           |     u     | Scroll up fast                                    |
|           Alt           |     d     | Scroll down fast                                  |
|           Alt           |     a     | Increment background transparency by 5%           |
|           Alt           |     s     | Decrement background transparency by 5%           |
