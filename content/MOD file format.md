#Mod
 [wiki](https://en.wikipedia.org/wiki/MOD_(file_format) "MOD (file format)")
 >**MOD** is a computer [file format](https://en.wikipedia.org/wiki/File_format "File format") used primarily to represent [music](https://en.wikipedia.org/wiki/Music "Music"), and was the first [module file](https://en.wikipedia.org/wiki/Module_file "Module file") format. MOD files use the “.MOD” [file extension](https://en.wikipedia.org/wiki/File_extension "File extension"), except on the [Amiga](https://en.wikipedia.org/wiki/Amiga "Amiga") which doesn't rely on filename extensions; instead, it reads a file's header to determine filetype. A MOD file contains a set of _instruments_ in the form of [samples](https://en.wikipedia.org/wiki/Sampling_(music) "Sampling (music)"), a number of _patterns_ indicating how and when the samples are to be played, and a list of what patterns to play in what order.

## History

> The first version of the format was created by [Karsten Obarski](https://en.wikipedia.org/wiki/Karsten_Obarski "Karsten Obarski") for use in the [Ultimate Soundtracker](https://en.wikipedia.org/wiki/Ultimate_Soundtracker "Ultimate Soundtracker"), [tracker](https://en.wikipedia.org/wiki/Tracker_(music_software) "Tracker (music software)") software released for the [Amiga](https://en.wikipedia.org/wiki/Amiga "Amiga") computer in 1987. The format has since been supported by hundreds of [playback programs](https://en.wikipedia.org/wiki/List_of_Amiga_music_format_players "List of Amiga music format players") and dozens of [other trackers](https://en.wikipedia.org/wiki/List_of_audio_trackers "List of audio trackers").

> The original version of the MOD format featured four channels of simultaneous audio playback, corresponding to the capabilities of the [original Amiga chipset](https://en.wikipedia.org/wiki/Original_Amiga_chipset#Paula "Original Amiga chipset"), and up to 15 instruments.

> Later variations of the format have extended this to up to 32 channels and 31 instruments.

> The format was designed to be directly playable on the Amiga without additional processing: for example, samples are stored in 8-bit [PCM](https://en.wikipedia.org/wiki/Pulse-code_modulation "Pulse-code modulation") format ready to be played on the Amiga [DACs](https://en.wikipedia.org/wiki/Digital-to-analog_converter "Digital-to-analog converter"), and pattern data is not packed. Playback required very little [CPU](https://en.wikipedia.org/wiki/CPU "CPU") time on an Amiga, and many games used MOD files for their [background music](https://en.wikipedia.org/wiki/Video_game_music "Video game music").

> A common misconception is that the [magic number](https://en.wikipedia.org/wiki/Magic_number_(programming) "Magic number (programming)") "M.K." in the 0x438 offset of MOD files are the initials of Mahoney and Kaktus, two prominent Amiga demomakers at the time, who played an important part in the popularity of the format. They in fact stand for the initials of [Michael Kleps](https://en.wikipedia.org/w/index.php?title=Michael_Kleps&action=edit&redlink=1 "Michael Kleps (page does not exist)") a.k.a. Unknown / DOC, another developer of the format.

> After the Amiga's production ceased, the MOD format has had continued popularity in the [Demoscene](https://en.wikipedia.org/wiki/Demoscene "Demoscene") and as background music for [independent video games](https://en.wikipedia.org/wiki/Independent_video_games "Independent video games") and [Chiptunes](https://en.wikipedia.org/wiki/Chiptune "Chiptune"). It is not uncommon to hear MOD music in [keygens](https://en.wikipedia.org/wiki/Keygen "Keygen") either.

## Format overview
> A pattern is typically represented in a sequencer [user interface](https://en.wikipedia.org/wiki/User_interface "User interface") as a table with one column per channel, thus having four columns – one for each Amiga hardware channel. Each column has 64 rows.

> A cell in the table can cause one of several actions to happen on its column's channel when its row's time is reached:

> - Start an instrument playing a new note in this channel at a given volume, possibly with a special effect applied on it
> - Change the volume or special effect being applied to the current note
> - Change pattern flow; jump to a specific song or pattern position or loop inside a pattern
> - Do nothing; any existing note playing in this channel will continue to play

> An instrument is a single sample along with an optional indication of which portion of the sample can be repeated to hold a sustained note.

## Timing
> In the original MOD file the minimum time frame was 0.02 seconds, or a "[vertical blanking](https://en.wikipedia.org/wiki/Vertical_synchronization "Vertical synchronization")" (VSync) interval, because the original software used the VSync timing of the monitor running at 50 Hz (for [PAL](https://en.wikipedia.org/wiki/PAL "PAL")) or 60 Hz (for [NTSC](https://en.wikipedia.org/wiki/NTSC "NTSC")) for timing.

> The rate at which pattern data is played is defined by a _speed setting_. Each row in the pattern data lasts one vertical blanking (or 0.02 seconds) times the current speed setting. The speed setting varied from 1 to 255. In later versions of the format, the vertical blanking was replaced with an adjustable time period staying in the range [0.01, 0.078] seconds. The old speed setting command was replaced with a new one that was used to change both the old speed setting and the new adjustable time period. Unfortunately, some of the old functionality was broken, because the new speed setting command had an identical code value to the old command. Values in the range [1, 31] were interpreted as the old speed settings, but other values were regarded as modifications to the adjustable time period. Hence, values in the range [32, 255] used in some old songs broke in new versions of the player.

> Further information on the MOD format can be found at the alt.binaries.sounds.mods FAQ.

## Other formats that use the MOD extension
> MOD is the [file extension](https://en.wikipedia.org/wiki/File_extension "File extension") for several other applications:

> - The [video file format](https://en.wikipedia.org/wiki/MOD_(video_format) "MOD (video format)") used on many digital [camcorders](https://en.wikipedia.org/wiki/Camcorder "Camcorder"), such as the JVC Everio, the Canon FS100 and the Panasonic D-Snap SD-card camcorders.
> - Game modules in [Neverwinter Nights](https://en.wikipedia.org/wiki/Neverwinter_Nights_(2002_video_game) "Neverwinter Nights (2002 video game)").
> - [AMPL](https://en.wikipedia.org/wiki/AMPL "AMPL") model files.
> - Old [phpBB](https://en.wikipedia.org/wiki/PhpBB "PhpBB") modification templates.
> - Module files in [Femap](https://en.wikipedia.org/wiki/Femap "Femap")
> - The extension for the [binary](https://en.wikipedia.org/wiki/Binary_file "Binary file") variant of the [Wavefront .obj format](https://en.wikipedia.org/wiki/Wavefront_.obj_file "Wavefront .obj file").
> - The extension for some games using the Vassal game engine.
> - The extension for [Fortran](https://en.wikipedia.org/wiki/Fortran "Fortran") module files.
> - The extension for [legacy Visual Basic](https://en.wikipedia.org/wiki/Visual_Basic_(classic) "Visual Basic (classic)") module files, for versions before the release of [Visual Basic .NET](https://en.wikipedia.org/wiki/Visual_Basic_.NET "Visual Basic .NET").
> - The extension for [Go](https://en.wikipedia.org/wiki/Go_(programming_language) "Go (programming language)") module files, used for package versioning.
> - Module for ABB Robotics IRC5 and S4 robot controllers. Contains robotic motion programs written in the language RAPID.
> - [Lanner](https://en.wikipedia.org/wiki/Lanner_Group_Ltd "Lanner Group Ltd") WITNESS simulation software model files
> - [Paradox Development Studio](https://en.wikipedia.org/wiki/Paradox_Development_Studio "Paradox Development Studio") uses a ".MOD" format for user-created modifications of their games.
> - DND adventure modules for [Fantasy Grounds](https://en.wikipedia.org/wiki/Fantasy_Grounds "Fantasy Grounds"), a virtual tabletop application.
> - [GNU GRUB](https://en.wikipedia.org/wiki/GNU_GRUB "GNU GRUB") boot modules (when found in /boot)

