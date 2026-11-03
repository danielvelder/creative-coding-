Micro:bit Album: Yot Club Chiptune Player

A pocket-sized "album" for the BBC micro:bit v2. It plays chiptune versions of three Yot Club songs, lets you switch songs with a button, and shows a small spinning record on the LED screen while the music plays.

Student: Daniel Velder (26122073) Subject: 52685 Creative Coding, Assessment 2: Code Prototype Project (UTS) Language / environment: MakeCode Python (Microsoft MakeCode for micro:bit)

Why I made it

Earlier this year I tried to order a Yot Club vinyl as a gift, and it was lost in the post. This project is a small tribute: a device I can hold in my hand that plays the songs I wanted to share. It is not a 1:1 reproduction of the recordings. It is a chiptune-style tribute played through the micro:bit speaker.

Songs
#	Song	Notes
1	Japan	Main riff, written from a guitar tab
2	Fly Out West	Main riff, written from a guitar tab
3	U Dont Kno Me	Placeholder melody (short, simplified)

The notes come from the tabs, but the rhythms are my own approximations, so the songs sound like a loose chiptune take rather than the originals.

Controls
Button	What it does
A	Play the selected song. Press again to stop.
B	Stop the music and move to the next song. The song's name scrolls across the screen.

While the music plays, the 5x5 LED screen shows a dot circling the middle pixel, like a spinning record.

How to run it
Go to makecode.microbit.org and click New Project.
Switch from Blocks to Python using the toggle at the top of the editor.
Delete the default code, then copy everything from yotclub_player.py and paste it in.
Connect your micro:bit v2 with a USB cable and click Download (or use Connect device to download directly).
When it starts, the first song name ("Japan") scrolls on the screen. Press A to play and B to change song.

You can also test it without hardware using the on-screen micro:bit simulator in MakeCode, although the sound and button feel are best on the real device.


