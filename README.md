##j2c

__joy2chord alterations__

joy2chord written by Nathanael Anderson wirelessdreamer (AT)
gmail (DOT) com.

As [wirelessdreamer][1] suggested joysticks are cheaper
than chorded keyboards. Keyboards are perhaps
cheaper and much more common. So modded it.

Have setup to allow 10 key operation for
[asetnoip][2]. [Asetniop][2] config files are for
chordvak the dvoriak version and are modified from
the default layout. The default layout seems
optimized for tablets but would get in the way of
coding with autocomplete and wastes some keys. For
example: ! (shift-1). Which isn't really a waste
as it gets you a one chord !, but this doesn't
balance for me on the key real estate. Have not
implemented auto complete but if I do may use a
double shift or shift space. The single shift has
problems for things like camelCase which probley
only coders use. Could perhaps have an
enable/disable autocomplete or a seperate
mode. Replaced the ! ( ) ?  keys with = [ ] /
respectively. Also added numbers/modifier keys to
thumb chords*:

numbers                 | others
---                     | ---
rthumb rpinky-1         | lthumb rpinky-Alt
rthumb rring-2          | lthumb rring-Control
rthumb rmiddle-3        | lthumb rmiddle-Insert
rthumb rindex-4         | lthumb lmiddle-Tab
lthumb lindex-5         | lthumb lring-Escape
lthumb rindex-6         | lthumb lpinky-Super
rthumb lindex-7         |
rthumb lmiddle-8        | lpinky lindex rindex-`
rthumb lring-9          | lindix rindex rpinky-\
rthumb lpinky-0         |


no realestate for ` or \ so 3key chords:

\* This changed recently because I'm a horrible
  awful person mostly also with the dvorak keys
  there seems to have been an attempt to
  implement asetniop keys using muscle memory of
  the key in standard layout mode. This is an
  attempt to conform with that. This applies to
  the changes for ` and \ as well.

have added a new mode for numbers, fn and
directional keys:

- lpinky lindex lthumb rthumb rindex-mode 2 (#,fn,dir)
- lpinky lring lindex lthumb-mode 1 (base mode)

mode 2

numbers             || function                      || others
---                 ||---                            || ---
rpinky           | 1 | rthumb rpinky            | f1  | lindex lring-home
rring            | 2 | rthumb rring             | f2  | lindex lmiddle-end
rmiddle          | 3 | rthumb rmiddle           | f3  | lindex rindex-pgup
rindex           | 4 | rthumb rindex            | f4  | lindex rmiddle-pgdn
lthumb lindex    | 5 | lpinky lindex            | f5  |
lthumb rindex    | 6 | lpinky rindex            | f6  | lring rindex-left
lindex           | 7 | rthumb lindex            | f7  | lring rmiddle-up
lmiddle          | 8 | rthumb lmiddle           | f8  | lring rring-down
lring            | 9 | rthumb lring             | f9  | lring rpinky-right
lpinky           | 0 | rthumb lpinky            | f10 | 
                 |   | pinky lring              | f11 | 
                 |   | pinky lmiddle            | f12 | 


Shift, Space, Enter, Alt, Control, Insert, Tab,
Super, =, / and . are all the same as in mode
1. Escape is available in config file but
commented out as it just caused me problems.

The buttons may need to be altered for your
keyboard. I have it set for numpad homerow(456+)
and left arrow for thumb for right hand. The left
hand is on its home row(asdf) and the space key is
shift.

The other config files you should be able to
figure out if you read the files. There is some
wierdness with the dvorak layout that I use for
the keyboard that requires some of the files to
mirror dvorak. Most have versions of both. These
layouts are my own based on [english letter
frequency][3]. And could likely be better
optimised. [Asetniop][2] has got me thinking...

Added the -f option for file. This is currently
the only way to use a keyboard on archlinux I use
/dev/input/by-id/* as the names are descriptive.

Working for my dell keyboard and the apple usb
keyboard but must first disable the device. on
archlinux execute:

>xinput -list

get the keyboard id you want to use and replace
the _num_ in the command below.

>xinput -disable _num_

otherwise see [joy2chords][1] documentation or the
config files.

[1]: http://joy2chord.sourceforge.net/
[2]: http://asetniop.com/
[3]: https://en.wikipedia.org/wiki/Letter_frequency
