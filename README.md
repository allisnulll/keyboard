# My Keyboard Config
*(part of my [dotfiles](https://github.com/allisnulll/dotfiles))*

This is the **[Kanata](https://github.com/jtroo/kanata)** config I created while learning the **[Graphite](https://github.com/rdavison/graphite-layout)** layout. Looking at the [configuration guide](https://jtroo.github.io/config.html#multi) I realized there was a lot more I could do than just change the positions of the letters, so I added the following features:

## Features
- Home Row Mods
- Swappable base layers for toggling features on and off
- Navigation, Numrow, Numpad, Symbol, and Function layers
- Access to `hjkl;'` or `yhaei;` keys with the Vim layer
- Repeat keys *(never press the same key twice in a row)*
- Mirror layers for when one-handed
- One-shot shift keys
- Caps-word key
- Custom Nav layer for video speed controller browser extension

## Why Program your Keyboard?
This is a highly overlooked part of workflow optimization. It's one thing to make every function on your computer just a few keystrokes away, but it's another to make those keystrokes physically closer to your fingers. After all, the entire point of a *Vim/Tmux/TilingWM* workflow is to minimize physical movement, right?

Some try to solve this by buying expensive keyboards that feel better to type on. That's cool and all, but it doesn't matter if you're still reaching for distant keys, straining your hands. In the end what actually ends up improving your experience the most is the reduced amount of physical keys forcing you to create your own keyboard layout.

***With a well configured keyboard layout it is possible to never reach for a single key ever again!***

*The guiding principle is simple*: move the key to your finger, instead of the finger to the key.

For me, **Home Row Mods** are the pinnacle of this philosophy. No reaching to the corner or edge of your keyboard anymore, limitless possibilities.

#### Other features that massively improve my ergonomics:
- **Repeat Keys**: You know how *ThePrimeagen* uses `Vd` instead of `dd`? Do that for everything! Just put a couple of repeat keys next to your space bar, and you'll never have to press the same physical key twice in a row ever again! *(This is what really made HRM timings usable for me and has improved my typing experience overall)*
- **Numrow Layer**: A lot of people make a numpad, but just moving the numbers up-top just two rows down instead is a real game-changer. Pair that with *HMR*, and you can zip precisely to any relative line, jump between *Tmux* windows, workspaces, and even *Chromium* tabs.
- **Symbol Layer**: Do this however you want but the main thing for me is putting `<[{()}]>` directly on the home row, very intuitive. I am a programmer, so I like to place certain keys opposite each other such as `&` and `|`, or `^` and `$`.
- **Navigation Layer**: Everybody focuses on the arrow keys, but *PgUp* and *PgDn* are underrated. They not only serve as an extra pair of scroll keys, but are also often bound to useful shortcuts in external programs, I use them all the time to move around tabs in *Chromium*.
- **Alternate Letter Layout**: I use *Graphite*, and honestly, it just feels better than *Qwerty*. My typing is smoother, more accurate, and the only real advantage *Qwerty* has at this point is the years of built-up muscle memory. After half a year (at the point of writing this) using it as my main layout, the gap in muscle memory has become marginal, and I can get 70-80wpm on *english10k* consistently which is something I couldn't do on Qwerty.

    Here I am typing 100wpm switching layouts mid-type to prove you don't forget *Qwerty* if you train a bit: https://www.youtube.com/watch?v=ocN9lPpIuj8

## **Vanilla Thinkpad T480s Keyboard**:

![thinkpad-keyboard-layout.png](assets/thinkpad-keyboard-layout.png)
*(Swapped Fn and Ctrl in the BIOS)*

```
    esc  f1  f2  f3  f4  f5  f6  f7  f8  f9  f10  f11  f12 home end  ins  del
    grv  1    2    3    4    5    6    7    8    9    0    -    =         bspc
    tab       q    w    e    r    t    y    u    i    o    p    [    ]    \
    caps      a    s    d    f    g    h    j    k    l    ;    '         ent
    lsft      z    x    c    v    b    n    m    ,    .    /              rsft
    lctl wkup lmet lalt           spc            ralt prnt rctl pgup up   pgdn
                                                                left down rght
```
This is the base keyboard layout I am working with. All the layers are designed for the layout of the ***ThinkPad t480s*** laptop. The **Kanata** key names can be found [here](https://github.com/jtroo/kanata/blob/main/parser/src/keys/mod.rs).

## Base Layers:
There are six possible base layers:
- *graphite*
- *qwerty*
- *graphite-no-home-row*
- *qwerty-no-home-row*
- *graphite-home-row*
- *qwerty-home-row*

These are all combinations of different letter layouts as well as varying amounts of custom keys. The goal of this is to improve the ability to keep your fingers on the home row, while still retaining all the regular functionality the regular keyboard layout provides.

### **Graphite**
```
    _    _   _   _   _   _   _   _   _   _   _    _    _   @hmr @lyt @rst _
    @~   _    _    _    _    _    _    _    _    _    _    _    _         _
    _         b    l    d    w    z    '    f    o    u    j    _    _    _
    _         n    r    t    s    g    y    h    a    e    i    ;         _
    _         q    x    m    c    v    k    p    _    _    _              _
    _    _    _    _              _              _    _    rmet _    _    _
                                                                _    _    _
```
This is what I change from the vanilla layer to get a **Graphite** layout. I like to keep the symbols the same as in **Qwerty**.

The top-right keys are responsible for base layer switching:
- *hmr*:
    * **Double-tap** = Toggle between *graphite-home-row* & *graphite* or *qwerty-home-row* & *qwerty*
    * **Shift + Double-tap** = Enter *graphite-no-home-row* or *qwerty-no-home-row*
- *lyt*:
    * **Double-tap** = Toggle between *graphite-home-row* & *qwerty-home-row* or *graphite* & *qwerty* or *graphite-no-home-row* & *qwerty-no-home-row*
- *rst*:
    * **Double-tap** = Reload Kanata, useful for debugging config file.

I also add a couple minor changes:
- Swapped `` ` `` and `~`
- Remapped *rctl* to *rmet*

### **Special Keys**
```
    _    _   _   _   _   _   _   _   _   _   _    _    _   _    _    _    _
    _    _    _    _    _    _    _    _    _    _    _    _    _         _
    @mir      _    _    _    _    _    _    _    _    _    _    _    _    @mir
    @md1      _    _    _    _    _    _    _    _    _    _    @md2      @md3
    @lsf      _    _    _    _    _    _    _    _    _    _              @rsf
    _    _    _    @md4           _              @md5 _    rmet _    _    _
                                                                _    _    _
```
This is what I change from the vanilla layer to get all the features besides home row mods:
- *md1*:
    * **Tap** = escape key
    * **Hold** = [nav layer](#Navigation)
    * **Double-tap** = [custom nav layer](#Custom-Navigation-Layer)
    * **Shift + tap** = *[cw](#Navigation)*
- *md2*:
    * **Tap** = normal key
    * **Hold** = [numrow layer](#Numrow)
    * **Double-tap** = [numpad layer](#Numpad)
- *md3*:
    * **Tap** = repeat key
    * **Hold** = [function layer](#Function)
- *md4*:
    * **Tap** = repeat key
    * **Hold** = [vim layer](#Vim)
- *md5*:
    * **Tap** = enter key
    * **Hold** = [nav layer](#Navigation)
- *lsf & rsf*:
    * **Tap** = One-shot shift
    * **Hold** = [sym layer](#Symbol)
- *mir*:
    * **Tap** = normal key
    * **Hold** = [mirror layer](#mirror-layers)

### **Home Row Mods**
```
    _    _   _   _   _   _   _   _   _   _   _    _    _   _    _    _    _
    _    _    _    _    _    _    _    _    _    _    _    _    _         _
    _         _    _    _    _    _    _    _    _    _    _    _    _    _
    _         @hr1 @hr2 @hr3 @hr4 _    _    @hr5 @hr6 @hr7 @hr8 @md2      _
    _         _    _    _    _    _    _    _    _    _    _              _
    _    _    _    _              _              _    _         _    _    _
                                                                _    _    _
```
Finally, the layout is completed with the inclusion of home row mods. I am using **[GASC](https://precondition.github.io/home-row-mods#gasc)** home row mods which means the order is *Meta*, *Alt*, *Shift*, *Ctrl*:
- *hr1-8*:
    * **Tap** = normal key
    * **Hold** = modifier key
    * **Double-tap** = normal key *(useful for regular hold key behavior when desired)*

## Sub Layers:
The combination of home row mods and sub-layers are what truly turn this layout from requiring fingers to move to keys, to requiring fingers to press keys already moved to them.

This is because while holding modifiers you can navigate to whatever layers you want using your other fingers making it easy to reach any keyboard shortcut imaginable.

> **NOTE:** A few of the layers here only change one side of the keyboard allowing the other hand to hold down any desired modifiers while inside the layer. \
This makes it look like layers which take up both sides of the keyboard cannot be combined with modifiers, this is not the case. \
To achieve the same effect, simply hold down modifiers before entering the layer.

### **Navigation**
```
    caps nlck slck _   _   _   _   _   _   _   _   _   _   _    _    _    _
    @cw  _    home up   end  _    _    _    _    @brd @bru vold volu      mute
    @tb1      ent  left down rght _    mwl  mwd  mwu  mwr  _    prev next pp
    _         tab  ins  pgup pgdn _    _    _    _    _    _    _         _
    _         _    _    _    _    _    _    _    _    _    _              _
    _    _    _    del            bspc           _    menu _    _    _    _
                                                                _    _    _
```
Provides easy access to navigation keys, as well as other useful keys.

- *cw*: Caps-word key to capitalize the next typed word.
- *tb1*: **Ctrl+Tab** for easy access when changing tabs in web browser. *(tb2 in [custom nav layer](#Custom-Navigation-Layer))*
- *brd*: Lowers brightness. Combine with control to lower temperature.
- *bru*: Raises brightness. Combine with control to raise temperature.
- Access to useful keys like enter and tab, as well as backspace and delete.
- Access to media keys as well as brightness keys
- Access to some minorly useful mouse keys as well as the regular lock keys just in case.

The arrow keys ended up there initially to avoid keyboard ghosting, but now, I have grown to like having them higher up. It feels natural to move the hand there because it is in the same position relative to the *CapsLock* button as the Home Row is to the *Shift* button. Plus you get easy access to *Tab* and the *PgUp*, *PgDn* buttons.

### **Numrow**
```
    _    _    _    _   _   _   _   _   _   _   _   _   _   _    _    _    _
    _    _    _    _    _    _    _    _    _    _    _    _    _         _
    _         _    _    _    _    _    _    _    _    _    _    _    _    _
    _         1    2    3    4    5    6    7    8    9    0    _         _
    _         _    _    _    _    _    _    _    _    _    _              _
    _    _    _    _              _              _    _    _    _    _    _
                                                                _    _    _
```
Moves the numbers at the top of the keyboard down to your fingers, so you don't have to reach for them. This makes a lot of shortcuts for moving things precisely way easier to type, making this one of the most useful layers for increasing productivity.

With this layer, commands you wouldn't ordinarily do such as precisely jumping between lines in *Vim* or switching to specific tabs or workspaces now become possible to do without thinking.

### **Symbol**
```
    _    _    _    _   _   _   _   _   _   _   _   _   _   _    _    _    _
    _    _    _    _    _    _    _    _    _    _    _    _    _         _
    _         _    _    @~   @&   @!   @#   @|   grv  _    _    _    _    _
    _         @<   [    @{   @op  -    @_   @cp  @}   ]    @>   _         _
    _         =    _    @@   \    @^   @$   @%   @+   @*   =              _
    _    _    _    _              _              _    _    _    _    _    _
                                                                _    _    _
```
Symbol layer with access to all the bracket types by finger. Intuitive layout for programmers with `&` opposite `|`, and `^` opposite `$`.
- *op*: Opening parenthesis
- *cp*: Closing parenthesis

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

### ***Mirror Layers***
##### Graphite
```
    _    _   _   _   _   _   _   _   _   _   _    _    _   _    _    _    _
    _         _    _    _    _    _    _    _    _    _    _    _         _
    _         j    u    o    f    '    z    w    d    l    b    _    _    _
    _         i    e    a    h    y    g    s    t    r    n    _         _
    _         /    .    ,    p    k    v    c    m    x    q              _
    _    _    _    _              _              _    _    _    _    _    _
                                                                _    _    _
```

##### Qwerty
```
    _    _   _   _   _   _   _   _   _   _   _    _    _   _    _    _    _
    _         _    _    _    _    _    _    _    _    _    _    _         _
    _         p    o    i    u    y    t    r    e    w    q    _    _    _
    _         ;    l    k    j    h    g    f    d    s    a    _         _
    _         /    .    ,    m    n    b    v    c    x    z              _
    _    _    _    _              _              _    _    _    _    _    _
                                                                _    _    _
```

Mirrors the letter so that the letters from one side can be accessed in the other. Access to special keys and **HRM** are maintained, meaning that using this layer you can do many operations one handed.

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
A mask into the opposite layout for those six keys on the right side of the keyboard commonly used for **Vim Motions**. This removes a major downside to using alternate keyboard layouts for **Vim** users.
- If *graphite* then `hjkl;'`
- If *qwerty* then `yhaei;`

### **Numpad**
```
    _    _    _    _   _   _   _   _   _   _   _   _   _   _    _    _    _
    _    @ch8 @ch4 @ch2 @ch1 _    _    _    @ch8 @ch4 @ch2 @ch1 _         _
    _         _    _    _    _    _    =    kp7  kp8  kp9  @n+  _    _    _
    _         _    _    _    _    _    kp0  kp4  kp5  kp6  @n*  _         _
    _         _    _    _    _    _    @.   kp1  kp2  kp3  @n^            _
    _    _    _    _              _              _    _    _    _    _    _
                                                                _    _    _
```
Customized numpad:
- `+` shifts to `-`
- `*` shifts to `/`
- `^` shifts to `%`
- `.` shifts to `,`
- *ch1-8*: Random binary chord config I found in the Kanata docs that I never use but I think is cool.

I never really use this anymore ever since adding the [numrow](#Numrow) layer and updating the [symbol](#Symbol) layer

### **Custom Navigation Layer**
Another mask layer for using Video Speed Controller Chromium extension
```
    _    _    _    _   _   _   _   _   _   _   _   _   _   _    _    _    _
    _    _    _    _    _    _    _    _    _    _    _    _    _         _
    @tb2      q    w    e    r    _    _    _    _    _    _    _    _    _
    _         a    s    d    f    g    _    _    _    _    _    _         _
    _         _    _    _    v    b    _    _    _    _    _              _
    _    _    _    _              _              _    _    _    _    _    _
                                                                _    _    _
```
This is what I use when watching YouTube while using a **Graphite** layout.  
`f` key is used for fullscreen.

![browser-extension.avif](assets/browser-extension.avif)

## External Config
- *kanata.service* makes it so you don't have to manually launch **Kanata** every system start.
    * On **Hyprland** add this line to reliably start the service on startup:
    ```Hyprlang
    exec-once = systemctl --user start kanata.service
    ```
- Whenever the layout is switched a script is run that changes the directional keymaps for my *Hyprland*, *Tmux*, and *Rofi* configs.
    * The idea behind the script is to have a patch file generated beforehand using `git diff` that is then applied by the script.
    * Script file can be found [here](https://github.com/allisnulll/dotfiles/blob/main/scripts/graphite2qwerty.sh).
    * Patch file can be found [here](https://github.com/allisnulll/dotfiles/blob/main/patches/graphite2qwerty.patch).
- *kanata.service* makes it so you don't have to manually launch **Kanata** every system start. *(Stopped working)*
```zsh
# Kanata
alias kn="kanata -c ~/kanata/kanata.kbd --log-layer-changes"
alias knd="kanata -dc ~/kanata/kanata.kbd --log-layer-changes"
alias kns="systemctl --user stop kanata"
alias knl="systemctl --user status kanata"
alias knr="systemctl --user daemon-reload && systemctl --user restart kanata"
```
- *zippy.txt* has chords for frequently used text. I never use this tbh, but mine looks something like this:
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

### Useful Keybind Examples:
- *Nav layer provides easy access to useful shortcuts for navigation such as*
    * **Chromium Browser**:
        + **Ctrl+PgUp *or* Ctrl+PgDn**: Jump to next or previous tab
            1. Hold `j` for ctrl
            2. Hold `CapsLock` to enter Nav
            3. Press `f` or `t` for PgUp or PgDn
        + **Ctrl+Shift+PgUp *or* Ctrl+Shift+PgDn**: Move tab left or right
            1. Hold `j` for ctrl
            2. Hold `k` for shift
            3. Hold `CapsLock` to enter Nav
            4. Press `f` or `t` for PgUp or PgDn
        + **Alt+Left Alt+Right**: previous or next page
            1. Hold `l` for alt
            2. Hold `CapsLock` to enter Nav
            3. Press `w` or `r` to go between pages
        + **Ctrl+{number}**: Jump to specific tab
            1. Hold `f` or `j` for ctrl
            2. Hold `;` to enter Numrow
            3. Press any middle row key in order to jump to the corresponding numbered tab
