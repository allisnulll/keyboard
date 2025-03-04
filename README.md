# My Graphite Keyboard Layout
I decided to learn the **Graphite** keyboard layout and this is the **Kanata** config I ended up creating for my ***ThinkPad t480s*** laptop. *Part of my [dotfiles](https://github.com/allisnulll/.dotfiles) repo.*

## Features
- Toggleable Qwerty Layout
- Toggleable Home Row Mods *(using **GASC**: Meta, Alt, Shift, Ctrl)*
- Repeat keys *(never press the same key twice in a row)*
- Always have access to `hjkl;'` or `yhaei;` keys depending on your currently selected layout
- One-shot shift keys & dedicated caps-word key in nav layer
- Nav layers provide easy access to useful shortcuts for browser navigation such as:
    * **Ctrl+Tab *or* Ctrl+PgDn:** Jump to previous tab
    * **Ctrl+Shift+Tab *or* Ctrl+PgUp:** Jump to next tab
    * **Ctrl+Shift+PgDn:** Move tab right
    * **Ctrl+Shift+PgUp:** Move tab left
    * **Alt+Left:** previous page
    * **Alt+Right:** next page
- Changed `` ` `` to be `~` by default

## **Vanilla Laptop Keyboard**
```
    esc  f1  f2  f3  f4  f5  f6  f7  f8  f9  f10  f11  f12 home end  ins  del
    grv  1    2    3    4    5    6    7    8    9    0    min  eql       bspc
    tab       q    w    e    r    t    y    u    i    o    p    [    ]    \
    caps      a    s    d    f    g    h    j    k    l    ;    apos      ent
    lsft      z    x    c    v    b    n    m    ,    .    /              rsft
    lctl wkup lmet lalt           spc            ralt prnt rctl pgup up   pgdn
                                                                left down rght
```
**Kanata** key names can be found [here](https://github.com/jtroo/kanata/blob/main/parser/src/keys/mod.rs).

## Layers:

### Main Layer
Four possible main layers:
- *graphite-home-row*
- *graphite*
- *qwerty-home-row*
- *qwerty*

Three top-right keys are responsible for main layer switching:
- *hmr:* Double-tap to toggle home row & other special keys.
    * Toggles between *graphite-home-row* & *graphite* or *qwerty-home-row* & *qwerty*
- *lyt:* Double-tap to toggle keyboard layout:
    * Toggles between *graphite-home-row* & *qwerty-home-row* or *graphite* & *qwerty*
- *rst:* Double-tap to reload layout, useful for debugging.

### **Graphite**
```
    _    _   _   _   _   _   _   _   _   _   _    _    _   @hmr @lyt @rst _
    @~   _    _    _    _    _    _    _    _    _    _    _    _         _
    _         b    l    d    w    z    apos f    o    u    j    _    _    _
    _         n    r    t    s    g    y    h    a    e    i    ;         _
    _         q    x    m    c    v    k    p    _    _    _              _
    _    _    _    _              _              _    _    _    _    _    _
                                                                _    _    _
```
This is what I change from the vanilla layer to get the **Graphite** layout. I like to keep the symbols mostly the same as in **Qwerty**.

### **Home Row**
```
    _    _   _   _   _   _   _   _   _   _   _    _    _   @hmr @lyt @rst _
    @~   _    _    _    _    _    _    _    _    _    _    _    _         _
    _         _    _    _    _    _    _    _    _    _    _    _    _    _
    @md1      @hr1 @hr2 @hr3 @hr4 _    _    @hr5 @hr6 @hr7 @hr8 @md2      @md5
    @lsf      _    _    _    _    _    _    _    _    _    _              @rsf
    _    _    _    @md3           _              @md4 _    _    _    _    _
                                                                _    _    _
```
This is what I change from the vanilla layer to get my home row mods and other custom mod keys. I am using **[GASC](https://precondition.github.io/home-row-mods#gasc)** home row mods which means the order is *Meta*, *Alt*, *Shift*, and then *Ctrl*.
- *hr1-8:*
    * **Tap** = regular key
    * **Hold** = modifier key
    * **Double-tap** = regular key *(useful for regular hold key behavior when desired)*
- *md1:*
    * **Tap** = esc key
    * **Hold** = nav layer
    * **Double-tap** = custom nav layer
- *md2:*
    * **Tap** = regular key
    * **Hold** = num layer
    * **Double-tap** = regular key *(useful for regular hold key behavior when desired)*
- *md3:*
    * **Tap** = repeat key
    * **Hold** = function layer
- *md4:*
    * **Tap** = repeat key
    * **Hold** = vim layer
- *md5:*
    * **Tap** = enter key
    * **Hold** = nav layer
- *lsf & rsf:*
    * **Tap** = One-shot shift
    * **Hold** = sym layer

### **Navigation**
```
    caps nlck slck _   _   _   _   _   _   _   _   _   _   _    _    _    _
    @cw  _    ins  up   tab  _    _    _    _    brdn brup vold volu      mute
    @tb1      tab  left down rght _    _    mwu  mwd  mwl  mwr  prev next pp
    _         ent  _    home end  _    _    _    _    _    _    _         _
    _         _    _    pgup pgdn _    _    _    _    _    _              _
    _    _    _    del            bspc           _    _    _    _    _    _
                                                                _    _    _
```
Provides easy access to navigation keys, as well as other useful keys. Does not remove access to modifier keys on right side in order to allow for things like highlight or jump by word.
- *cw:* Caps-word key to capitalize the next typed word.
- *tb1:* **Ctrl+Tab** for easy access when changing tabs in web browser. *(tb2 in custom nav layer)*
- Access to useful keys like enter and tab, as well as backspace and delete.
- Access to media keys as well as brightness keys
- Access to some minorly useful mouse keys as well as the regular lock keys just in case.

### **Numpad**
```
    _    _    _    _   _   _   _   _   _   _   _   _   _   _    _    _    _
    _    @ch8 @ch4 @ch2 @ch1 _    _    _    @ch8 @ch4 @ch2 @ch1 _         _
    _         _    _    _    _    _    eql  kp7  kp8  kp9  @+   _    _    _
    _         _    _    _    _    _    kp0  kp4  kp5  kp6  @*   _         _
    _         _    _    _    _    _    @.   kp1  kp2  kp3  @^             eql
    _    _    _    bspc           _              _    _    _    _    _    _
                                                                _    _    _
```
Numpad with some custom keys.
- `+` shifts to `-`
- `*` shifts to `/`
- `^` shifts to `%`
- `.` shifts to `,`
- *ch1-8:* Random binary chord config I found in Kanata docs that I never use.

### **Symbol**
```
    _    _    _    _   _   _   _   _   _   _   _   _   _   _    _    _    _
    _    _    _    _    _    _    _    _    _    _    _    _    _         _
    _         _    _    @~   @&   @!   @#   @|   grv  _    _    _    _    _
    _         @<   [    @{   @op  -    @_   @cp  @}   ]    @>   _         _
    _         _    _    _    \    @$   @@   @%   _    _    _              _
    _    _    _    bspc           _              _    _    _    _    _    _
                                                                _    _    _
```
Symbol layer with access to all the bracket types by finger.

### **Function**
```
    _    _    _    _   _   _   _   _   _   _   _   _   _   _    _    _    _
    _    _    _    _    _    _    _    _    _    _    _    _    _         _
    _         @f12 @f7  @f8  @f9  _    _    _    _    _    _    _    _    _
    _         @f11 @f4  @f5  @f6  _    _    _    _    _    _    _         _
    _         @f10 @f1  @f2  @f3  _    _    _    _    _    _              _
    _    _    _    _              _              _    _    _    _    _    _
                                                                _    _    _
```
Function layer with easy access to F11 *(fullscreen toggle)* and F13-24 while using shift.

### **Vim**
```
    _    _    _    _   _   _   _   _   _   _   _   _   _   _    _    _    _
    _    _    _    _    _    _    _    _    _    _    _    _    _         _
    _         _    _    _    _    _    _    _    _    _    _    _    _    _
    _         _    _    _    _    _    @lft @dwn @up  @rgt @;   @'        _
    _         _    _    _    _    _    _    _    _    _    _              _
    _    _    _    _              _              _    _    _    _    _    _
                                                                _    _    _
```
Think of this layer as a mask into the opposite layout for those six keys on your right hand. Most useful when navigating in **NeoVim** while using **Graphite** layout.
- If *graphite* then `hjkl;'`
- If *qwerty* then `yhaei;`

### **Custom Nav Layer**
*(for using Video Speed Controller Chrome extension)*
```
    _    _    _    _   _   _   _   _   _   _   _   _   _   _    _    _    _
    _    _    _    _    _    _    _    _    _    _    _    _    _         _
    @tb2      q    w    e    r    _    _    _    _    _    _    _    _    _
    _         a    s    d    f    g    _    _    _    _    _    _         _
    _         _    _    _    v    b    _    _    _    _    _              _
    _    _    _    _              _              _    _    _    _    _    _
                                                                _    _    _
```
This is what I use when watching YouTube while using **Graphite** layout.  
`f` key is used for fullscreen.

![browser-extension.avif](assets/browser-extension.avif)

## External Config
- Whenever the layout is switched a script is run that changes the directional keymaps for my *Hyprland*, *Tmux*, and *Rofi* configs.
    * The idea behind the script is to have a patch file generated beforehand using `git diff` that then is applied using the script to change the config.
    * The script can be found [here](https://github.com/allisnulll/.dotfiles/blob/main/scripts/graphite2qwerty.sh).
- *kanata.service* makes it, so you don't have to manually launch **Kanata** every system start.
- *zippy.txt* has zippy chords for frequently used text. Mine looks something like this:
```txt
us 1	Username1
us 2	Username2
em e	email1@mail.com
em e 2	email2@mail.com
fi h	/home/username/
fi d w	/home/username/Downloads/
fi d c	/home/username/Documents/
fi d e	/home/username/Desktop/
fi p	/home/username/Pictures/
fi v	/home/username/Videos/
fi .	/home/username/.dotfiles/
fi m	/home/username/Music/
```
- I have a few **Zsh** aliases set up for convenience:
```zsh
# Kanata
alias kn="kanata -c ~/kanata/kanata.kdb --log-layer-changes"
alias knd="kanata -dc ~/kanata/kanata.kdb --log-layer-changes"
alias kns="systemctl --user stop kanata"
alias knl="systemctl --user status kanata"
alias knr="systemctl --user daemon-reload && systemctl --user restart kanata"
```
