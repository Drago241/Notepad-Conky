Notepad Conky Theme

This is a lightweight, minimalist "Notepad" theme for Conky that displays the contents of a text file directly on your desktop with a sleek, rounded-corner aesthetic.

Features:

    Dynamic Note Display: Automatically reads and displays text from a .notes file on your desktop.

    Rounded Corners: Uses a custom Lua script and Cairo graphics for a smooth, modern window shape.

    Text Wrapping: Automatically folds long lines of text to ensure they stay within the widget boundaries.

    Optimized Performance: Uses double buffering to prevent flickering and a specific text buffer size to handle longer notes.

File Structure

    notes.conkyrc: The main configuration file that defines the window behavior, fonts, and the command to fetch your notes.

    rounded.lua: A Lua script that draws the semi-transparent, rounded background using the Cairo library.

Setup Instructions

    Place the Files:
    Move the Notepad-conky folder to your Conky configuration directory, typically located at ~/.conky or at ~/.config/conky. 

    Create Your Notes File:
    The theme looks for a file named .notes You can create it by running touch <file path> or by simply creating a new file if you don't have one already.

    Install Dependencies:
    Ensure you have conky installed with Lua and Cairo support. You may also need the Inter font for the intended look (any font will work).

    Run the Theme:
    Launch the theme using the following command:
    Bash

    conky -c ~/.conky/Notepad-conky/notes.conkyrc or ~/.config/conky/Notepad-conky/notes.conkyrc

Configuration Details:
Setting	Description

Window Type:	
-Set to normal with hints to skip the taskbar and stay below other windows.
Transparency	
-Uses argb_visual for true transparency and a Lua hook for the background.
Note Source	
-Executes fold -s -w 40 <path to the notes file> every 5 seconds to update the text.

Background:	
-Rendered with a corner radius of 15 and a black opacity of 80%.
