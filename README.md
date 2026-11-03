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

Files in this repository
README.md           This file
yotclub_player.py   The full program (MakeCode Python), with comments
How the code works
songs: a list of dictionaries. Each song has a name and a melody (a list of note strings such as "bb3:0.5", meaning note, octave, and length in beats). Keeping the songs as data means a new song only needs one new dictionary.
current_track and playing: two variables that act as the program's memory. current_track is which song is selected, and playing is True or False.
play_current() / stop_playing(): start the selected melody in the background, or stop all sound and reset.
Button B handler: moves to the next song with (current_track + 1) % len(songs) so it wraps back to the first song after the last. The title scroll runs with control.in_background so button presses are not blocked.
Button A handler: a simple toggle. If playing, stop. Otherwise, play.
spin(): runs forever with basic.forever and, only while music is playing, shows the next of eight LED frames to make a dot circle the centre.

