# dub's Preonic keymap

This keymap is primarily based on the `smt` keymap, which is itself based on the default Preonic keymap, which in turn is derived from Planck's default.

Notable differences from the default are:

- **[Mod-Tap](https://github.com/jackhumbert/qmk_firmware/wiki#fun-with-modifier-keys) keys**

    - `Esc/Ctrl`

        I am experimenting with using Left Shift as a mod-tap key for Escape, similar to how I use the Enter key. It's set up like this on my Minivan, so in the interest of consistency...

    - `Enter/Shift`

        I use both the left and right shift keys when I type. When I want to modify a key with shift, I hold shift with the hand opposite the one typing the key. In the default keymap, Enter is where shift would be on a standard keyboard layout. Oh, muscle memory.

    - `Tab/Hyper` (Super+Ctrl+Shift+Alt)

        It's great to be able to use Tab as a custom modifier key. I tend to use [Hyper](http://brettterpstra.com/2012/12/08/a-useful-caps-lock-key/) commands for various OS-specific operations depending on what machine I'm working on.

    - `Backtick/Meh` (Ctrl+Shift+Alt)

        Why use backtick in the lower left corner? I use it as my tmux prefix key, so I need to type it more frequently than most people. Putting it on the base layer works well for me. The "Meh" mapping is just a less-cool "Hyper"; the same, just without Super.

Notable differences from the smt keymap are:

- Removed dvorak and colemak layout, I rely on OS support for those.
- Move the quote key one row upward and use that space for conventional space
  and shift keys.
- Remove audio support.
- Swap lower and raise because it makes more sense to me that way.
- Add swap hands support.

## Qwerty

```
,-----------------------------------------------------------------------------------.
|   `  |   1  |   2  |   3  |   4  |   5  |   6  |   7  |   8  |   9  |   0  | Bksp |
|------+------+------+------+------+------+------+------+------+------+------+------|
| Tab  |   Q  |   W  |   E  |   R  |   T  |   Y  |   U  |   I  |   O  |   P  |  '   |
|------+------+------+------+------+-------------+------+------+------+------+------|
| Esc  |   A  |   S  |   D  |   F  |   G  |   H  |   J  |   K  |   L  |   ;  |Enter |
|------+------+------+------+------+------|------+------+------+------+------+------|
| Shift|   Z  |   X  |   C  |   V  |   B  |   N  |   M  |   ,  |   .  |   /  |Shift |
|------+------+------+------+------+------+------+------+------+------+------+------|
|   `  | Ctrl | Alt  | GUI  |Lower |    Space    |Raise | Left | Down |  Up  |Right |
`-----------------------------------------------------------------------------------'
```

## Lower

As a developer, it makes the most sense for me to group all the commonly-used symbols that don't fit on the main layer. In particular, having the dual-column of parens-braces-brackets really helps a lot. I've also added cursorkeys to correspond to the arrows.

I haven't completely filled this layer, which leaves room for future mappings and macros.

```
,-----------------------------------------------------------------------------------.
|   ~  |   !  |   @  |   #  |   $  |   %  |   ^  |   &  |   *  |   (  |   )  | Del  |
|------+------+------+------+------+-------------+------+------+------+------+------|
|   ~  |   !  |   @  |   #  |   $  |   %  |   ^  |   &  |   *  |   (  |   )  | Del  |
|------+------+------+------+------+-------------+------+------+------+------+------|
|      |      |      |      |      |      |   _  |   ?  |   +  |   {  |   }  |  |   |
|------+------+------+------+------+------|------+------+------+------+------+------|
|      |      |      |      |      |      |   -  |   /  |   =  |   [  |   ]  |  \   |
|------+------+------+------+------+------+------+------+------+------+------+------|
|      |      |      |      |      |      |      |      | Home |PageDn|PageUp| End  |
`-----------------------------------------------------------------------------------'
```

## Raise

This is where I put the number row, a numpad cluster, function keys, and media controls. Like the "Lower" layer, the top row is redundant to help with Planck compatibility.

```
,-----------------------------------------------------------------------------------.
|   `  |   1  |   2  |   3  |   4  |   5  |   6  |   7  |   8  |   9  |   0  | Del  |
|------+------+------+------+------+------+------+------+------+------+------+------|
|   0  |   1  |   2  |   3  |   4  |   5  |   6  |   7  |   8  |   9  |   0  | Del  |
|------+------+------+------+------+-------------+------+------+------+------+------|
|   $  |  F1  |  F2  |  F3  |  F4  |  F5  |  F6  |   4  |   5  |   6  |      |      |
|------+------+------+------+------+------|------+------+------+------+------+------|
|      |  F7  |  F8  |  F9  |  F10 |  F11 |  F12 |   1  |   2  |   3  |      |      |
|------+------+------+------+------+------+------+------+------+------+------+------|
|      |      |      |      |      |             |      | Next | Vol- | Vol+ | Play |
`-----------------------------------------------------------------------------------'
```

## Adjust (Lower + Raise)

Utility layer. This is where I'd switch between Qwerty and Dvorak, ~~fool around with~~ adjust the audio/music settings, or put the Preonic into bootloader mode.

```
,-----------------------------------------------------------------------------------.
|  F1  |  F2  |  F3  |  F4  |  F5  |  F6  |  F7  |  F8  |  F9  |  F10 |  F11 |  F12 |
|------+------+------+------+------+------+------+------+------+------+------+------|
|      | Reset|      |      |      |      |      |      |      |      |      | Reset|
|------+------+------+------+------+-------------+------+------+------+------+------|
|      |      |      |Aud on|AudOff|AGnorm|AGswap|Qwerty|Colemk|Dvorak|      |      |
|------+------+------+------+------+------|------+------+------+------+------+------|
|      |Voice-|Voice+|Mus on|MusOff|MidiOn|MidOff|      |      |      |      |      |
|------+------+------+------+------+------+------+------+------+------+------+------|
|      |      |      |      |      |             |      |      |      |      |      |
`-----------------------------------------------------------------------------------'
```
