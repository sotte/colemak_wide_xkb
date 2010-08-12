============================
Colemak Wide Keyboard Layout
============================

This is an attempt to implement the colemak wide keyboard layout for Linux
(Ubuntu 10.04).

:Author:    Stefan Otte
:Started:   2010-08-12 Thu

What is Colemak Wide
====================

TODO

see http://forum.colemak.com/viewtopic.php?id=839&p=1 for more infos.


Layout
======

There are several 'wide' mods out there. So I just picked one I liked. Feel
free do edit and contribute. See the first link in the link section for more information.

::

      Colemak Standard
      ___________________________________________________________
      | ` | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 0 | - | = | BSp |
      -----------------------------------------------------------
      | Tab | q | w | f | p | g | j | l | u | y | ; | [ | ] | \ |
      -----------------------------------------------------------
      | BkSp | A | R | S | T | d | h | N | E | I | O | ' | Entr |
      -----------------------------------------------------------
      | Shift  | z | x | c | v | b | k | m | , | . | / | Shift  |
      -----------------------------------------------------------
      | Ctr | Wn | Alt | Space              | Alt | W | M | Ctl |
      -----------------------------------------------------------

      Wide
      _____________________________new___________________________
      | ` | 1 | 2 | 3 | 4 | 5 | 6 | = | 7 | 8 | 9 | 0 | - | BSp |
      -----------------------------------------------------------
      | Tab | q | w | f | p | g | [ | j | l | u | y | ; | ' | \ |
      -----------------------------------------------------------
      | BkSp | A | R | S | T | d | ] | h | N | E | I | O | Entr |
      -----------------------------------------------------------
      | Shift  | z | x | c | v | b | / | k | m | , | . | Shift  |
      -----------------------------------------------------------
      | Ctr | Wn | Alt | Space              | Alt | W | M | Ctl |
      -----------------------------------------------------------



How it works
============

*/usr/local/X11/xkb* is the folder with all layout related files. For the
colemak wide layout there is an *symbols/colemak_wide* file that contains the
layout.

Furthermore *rules/evdev.xml* list all available layouts. The layout section
was extended to include the new colemak_wide before the *</layoutlist>* tag::

    <layout>
        <configItem>
            <name>colemak_wide</name>
            <shortDescription>Colemak Wide</shortDescription>
            <description>Colemak Wide</description>
            <languageList><iso639Id>eng</iso639Id></languageList>
        </configItem>
    </layout>

colemak_wide is the name of the layout to include.



Install
=======

* make a backup of your /usr/share/X11/xkb folder.
* copy colemak_wide to /usr/share/X11/xkb/symbols/
* override /usr/share/X11/xkb/rules/evdec.xml
* System -> Pref. -> Keyboard
    * Language: English; choose "Colemak Wide"

TODO: write a script that installs the new layout


Links
=====

* http://forum.colemak.com/viewtopic.php?id=839&p=1
* http://ubuntuforums.org/showthread.php?t=633403
* http://people.uleth.ca/~daniel.odonnell/Blog/custom-keyboard-in-linuxx11 
* https://help.ubuntu.com/community/Howto:%20Custom%20keyboard%20layout%20definitions?action=fullsearch&context=180&value=linkto:"Howto:+Custom+keyboard+layout+definitions"
