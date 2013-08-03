##j2c

__joy2chord alterations__

As [wirelessdreamer][1] suggested joysticks are cheaper
than chorded keyboards. Keyboards are perhaps
cheaper and much more common. So modded it.

Have setup to allow 10 key operation for
[asetnoip][2].  Config files are for chordvak the
dvoriak version and are modified from the default
layout. The default layout seems optimized for
tablets but would get in the way of coding with
autocomplete and wastes some keys for !
(shift-1). Have not implemented auto complete but
if I do may use a double shift or shift
space. Replaced the ! ( ) ? keys with = [ ] /
respectively. Also added numbers/modifier keys to
thumb chords:

- rthumb rpinky-1
- rthumb rring-2
- rthumb rmiddle-3
- rthumb rindex-4
- rthumb lindex-5
- rthumb lmiddle-6
- rthumb lring-7
- rthumb lpinky-8
- lthumb lring-9
- lthumb lpinky-0
- lthumb rpinky-Alt
- lthumb rring-Control
- lthumb rmiddle-Insert
- lthumb rindex-Tab
- lthumb lindex-Escape
- lthumb lmiddle-Super

The buttons may need to be altered for your
keyboard. I have it set for numpad homerow(456+)
and left arrow for thumb for left hand. The right
hand is on its home row(asdf) and the space key is
shift.

Added the -f option for file currently the only
way to use a keyboard on archlinux I use
/dev/input/by-id/* as the names are descriptive.

Working for my dell keyboard and the apple usb
keyboard but must first disable the device. on
archlinux execute:

>xinput -list

get the keyboard id you want to use and replace
the _num_ in the command below.

>xinput -disable _num_

otherwise see [joy2chords][1] documentation.

[1]: http://joy2chord.sourceforge.net/
[2]: http://asetniop.com/
