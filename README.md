# vghs-mw3-plutonium (STILL IN THE WORKS)
VGHS for Modern Warfare 3 (Plutonium)

A fan-made mod that turns Call of Duty: Modern Warfare 3 team deathmatch
into a Video Game High School match: you play for VGHS Varsity against
rival school teams, with the logos, team names, and death effects to
match.

It runs on Plutonium (the MW3 "IW5" client) and uses Bot Warfare to fill
the other team with bots, so you can play it alone.

Video Game High School is an action-comedy web series from RocketJump,
created by Freddie Wong, Matthew Arnold, Will Campos and Brian Firenzi.
This mod is a fan tribute to their show, and all credit for the logos,
names, and world it uses goes to them.

  Fan project. Not affiliated with or endorsed by Video Game High
  School, RocketJump, Activision, Plutonium, or the Bot Warfare authors.
  See Credits and disclaimer.
  
<img width="450" height="250" alt="Screenshot 2026-10-19 111637" src="https://github.com/user-attachments/assets/54a03a57-f29d-4635-bf6f-20557bdeb483" />

<img width="450" height="250" alt="Screenshot 2026-10-19 111654" src="https://github.com/user-attachments/assets/06a0ef29-bdaf-4c46-875a-838b6ece115b" />

<img width="450" height="250" alt="Screenshot 2026-10-19 111705" src="https://github.com/user-attachments/assets/1a9f6cd8-32e9-4e82-a6f9-54d7a0d4233c" />

------------------------------------------------------------------------

What is in the mod

| Feature | File | Status | Scoreboard team names:
allies are VGHS Varsity, the opposing team gets a school name per
faction (all editable) | VGHS_Teams.gsc | Working | | Team emblems on
the scoreboard: your VGHS logo for the allied side, your Napalm logo for
the opposing side | faction_128_sas.iwi, faction_128_ussr.iwi,
faction_128_africa.iwi | Working for SAS, Spetsnaz and African Militia.
Not working for Inner Circle and GIGN (see Known issues) | | Yellow
Team - VGHS text in the bottom-right corner | vghs_logo.gsc | Working |
| Dead bodies get a faint pixel tint (orange-red for enemies, blue for
teammates) that flickers away | glitch_death.gsc | Experimental | | VGHS
logo picture in the top-right corner | vghs_logo_image.gsc and
headicon_dead.iwi | Experimental, needs an extra picture step | | FIELD
OF FIRE text in a corner | field_of_fire_logo.gsc | Optional | | Custom
main menu wallpaper | z_vghs_menu.iwd (you make it, see below) |
Optional | | Custom intro video | replaces the game's intro file in
storage\iw5\video (see below) | Optional, can reset after Plutonium
updates |

"Experimental" means it was built and tweaked but has not been fully
confirmed in every setup. If something misbehaves, just delete that
file.

------------------------------------------------------------------------

What you need

- Modern Warfare 3 (2011) on Steam, a legitimate copy
- Plutonium for MW3, from plutonium.pw
- Bot Warfare for Plutonium IW5 (the file z_svr_bots.iwd), installed in
  its own mods\bots folder
- Windows
- A plain-text editor such as Notepad, if you want to change names or
  settings

------------------------------------------------------------------------

Install, step by step

  Want a clean checklist with a checkpoint after every part? See
  INSTALL.md.

Step 1: Install MW3 and Plutonium

1.  Install MW3 through Steam.
2.  Install Plutonium from plutonium.pw and follow its setup to link
    your MW3 install.
3.  Launch MW3 through Plutonium once, then close it. This creates
    Plutonium's folders.

Step 2: Install Bot Warfare

This follows a Plutonium community guide for playing MW3 with bots. If
your Bot Warfare already works another way, you can keep that.

1.  Download Bot Warfare for Plutonium IW5. Make sure it is the
    Plutonium IW5 version, or it won't work. Unzip it. Inside is a file
    called z_svr_bots.iwd.
2.  Open %localappdata%\Plutonium\storage\iw5. Create a folder named
    mods, and inside it a folder named bots.
3.  Copy z_svr_bots.iwd into
    %localappdata%\Plutonium\storage\iw5\mods\bots\.
4.  The first time Bot Warfare runs, it adds more files and folders to
    that bots folder. That is normal.

Optional: name your bots: create a text file called bots.txt in the same
bots folder, with one bot name per line. Bot Warfare picks from those
names.

Updating: Plutonium updates sometimes break Bot Warfare until it is
updated too. To update, replace z_svr_bots.iwd with the new version.
Your bots.txt and other files in that folder stay.

Step 3: Open your Plutonium folder

1.  Press Windows key + R.
2.  Paste %localappdata%\Plutonium\storage\iw5 and press Enter.
3.  Inside it, make sure these two folders exist. Create them if they
    don't:
    - scripts\mp
    - images

You end up with these two locations:

    %localappdata%\Plutonium\storage\iw5\scripts\mp\    <- the .gsc script files go here
    %localappdata%\Plutonium\storage\iw5\images\        <- the .iwi picture files go here

Step 4: Install the core files

Copy these into scripts\mp:

- VGHS_Teams.gsc for the team names
- vghs_logo.gsc for the "Team - VGHS" text

Copy these into images:

- faction_128_sas.iwi is the VGHS logo (allied emblem)
- faction_128_ussr.iwi is the Napalm logo (Spetsnaz emblem)
- faction_128_africa.iwi is the Napalm logo (African Militia emblem)

Check that every script file ends in .gsc, not .gsc.txt. In File
Explorer, open the View menu and turn on File name extensions to see it.

Step 5 (optional): Install the extras

Copy into scripts\mp whichever you want:

- glitch_death.gsc for the death tint and flicker
- field_of_fire_logo.gsc for the FIELD OF FIRE text
- vghs_logo_image.gsc for the logo picture. This one also needs
  headicon_dead.iwi in images. It replaces the game's little skull icon
  with the VGHS logo.

Keep only one copy of each script. Two copies of the same file will
fight each other.

Step 6: Start a match

1.  Fully close MW3 and open it again. Scripts and pictures are only
    read when the game starts or a map loads, so a quick match restart
    can keep running the old files.
2.  Launch MW3 multiplayer through Plutonium.
3.  Open the console (the ~ key), type set fs_game mods/bots and press
    Enter. This loads Bot Warfare. Do it each time you start the game,
    before you begin a match.
4.  Start a Private Match with Team Deathmatch and pick a map.
5.  When you spawn in, a "welcome to Bot Warfare!" message shows in the
    killfeed for a few seconds. Press N to open the Bot Warfare menu.
    Move with W, A, S, D, select with Space, and press N to go back. Add
    bots from there. Its other options are in Bot Warfare's own README.

Step 7: Check it works

- Hold Tab to open the scoreboard. You should see VGHS Varsity and your
  logo on the allied side, and a school name and logo on the other.
- Look at the bottom-right corner for the yellow Team - VGHS text.
- If you installed glitch_death.gsc, shoot a bot. The body gets a faint
  tint and flickers away.

------------------------------------------------------------------------

Custom menu wallpaper and intro video (optional)

These are your own files, so they are not in the install steps above.
Here is how to add them.

Menu wallpaper

The main menu background is two pictures that Plutonium keeps in its
images folder: background_image.iwi and background_image_blur_less.iwi.
You replace both with your wallpaper.

1.  Turn your wallpaper into game pictures (.iwi). Follow Plutonium's
    texture guide at plutonium.pw/docs/modding/creating-textures. In
    short: convert the original background_image.iwi (in
    %localappdata%\Plutonium\storage\iw5\images\) to a .dds with the
    Texture Toolkit, put your wallpaper in at the same size, save it as
    a .dds with the same compression, and convert it back to .iwi.
    Matching the original's size and compression avoids garbled or black
    results.
2.  Make a second copy of the finished file, so you have both
    background_image.iwi and background_image_blur_less.iwi. Both can
    use the same wallpaper.
3.  Pack them into an .iwd.
    - Create a folder named images and put both .iwi files inside it.
    - Right-click the folder, choose Send to, then Compressed (zipped)
      folder.
    - Rename the .zip file to z_vghs_menu.iwd. Turn on File name
      extensions in File Explorer's View menu so you can change the
      ending.
4.  Install it. Put z_vghs_menu.iwd in
    %localappdata%\Plutonium\storage\iw5\.
5.  Fully close and reopen MW3. The new wallpaper shows on the main
    menu.

Why an .iwd and not loose files? Plutonium's launcher checks the files
in its images folder every time it starts. If one has changed, it
downloads the original back. An .iwd in storage\iw5 takes priority over
loose files and the launcher leaves it alone. The z_ at the start of the
name makes sure it loads after other archives.

The same trick works for the main menu music: put an mp3 named
plutonium_main.mp3 in a sound\music folder inside an .iwd.

Intro video

The intro that plays when the game starts is a video file in
%localappdata%\Plutonium\storage\iw5\video. The steps below come from
Plutonium community posts, so check them against your version.

1.  Open that video folder. Copy the original intro file somewhere safe
    as a backup, and note its exact name and file type.
2.  Make your video the same type of file, with the same name, as the
    original. If the original ends in .bik (Bink video), you will need a
    converter such as RAD Video Tools. Keep it short, since players sit
    through it every launch.
3.  Copy your file into the video folder, replacing the original.
4.  Start the game. The intro plays when it launches, and the Esc key
    skips it.

It can reset. Community posts report that Plutonium puts its original
intro back after an update, so you may have to copy your video in again.
Keep your file somewhere handy.

------------------------------------------------------------------------

Customize

Change the team names. Open VGHS_Teams.gsc in Notepad.

- The allies part is labeled DO NOT CHANGE. Leave it alone.
- The axis part (the opposing team) is labeled CHANGE THESE NAMES HERE.
  It has one name per faction. Change the text between the quotes, and
  keep the quotes.

| Faction | Where you see it | |---|---| | Inner Circle (Henchmen) | for
example on Rust | | Spetsnaz (OpFor) | for example on Favela | | P.M.C.
| | | African Militia | | | Any other opposing faction | a catch-all
name |

Change the death effect. At the start of the glitchOut section of
glitch_death.gsc you can change:

- tintAlpha: how strong the tint is (0 is invisible, 1 is solid)
- tintSize: the size of each pixel
- enemyColor and teamColor: the tint colors
- groundDelay, flickerCount, flickerStart: how long the body lies there
  and how fast it flickers away
- flickerBody: leave at 0. Hiding and showing a dead body can make it
  stand back up in this game.

Change the corner logo. In vghs_logo.gsc, change the text in
setText("Team - VGHS"), the color, or the size. In vghs_logo_image.gsc,
change logoSize and margin.

------------------------------------------------------------------------

Troubleshooting

| Problem | What to try | |---|---| | No bots, or no "welcome to Bot
Warfare!" message | Type set fs_game mods/bots in the console before
starting the match, and check that z_svr_bots.iwd is in
storage\iw5\mods\bots. | | Nothing changed | Fully close and reopen the
game. Check the file ends in .gsc and sits in scripts\mp. | | A script
error appears | Open the console (the ~ key). Red text names the file
and line. Delete that script, or send the message to the person who made
the mod. | | Team names didn't change | Make sure there is only one
VGHS_Teams.gsc, and that you replaced any older copy. | | An emblem is
blank or a checkered pattern | The game doesn't have that picture loaded
on that map. See Known issues. | | The game won't start | Move all your
added files out of scripts\mp and images, start the game, then add them
back one at a time. | | The menu wallpaper keeps going back to normal |
It must be inside an .iwd in storage\iw5, not loose in the images
folder. See the wallpaper steps. | | The wallpaper is black or garbled |
Rebuild the .iwi from the original background_image.iwi so the size and
compression match. | | The intro video went back to the original |
Plutonium restores it after updates. Copy your video into the video
folder again. |

------------------------------------------------------------------------

Known issues

- Inner Circle and GIGN emblems don't change (TEMP PLACEHOLDER IS ADDED). The picture file names the
  game uses for these two aren't known, and replacing faction_128_ic and
  faction_128_gign does nothing. The names in the game's settings don't
  always match the picture file names. The African Militia emblem shows
  this: the game calls it faction_128_af, but the file that works is
  faction_128_africa.
- A script can't fix those two. Pointing a team's emblem at a picture
  the map hasn't loaded shows a blank square or a checkered pattern.
- The logo picture in the corner depends on headicon_dead.iwi having the
  right file name. If it shows the original skull icon, the name is
  wrong.
- Best for offline and private matches. It has not been tested on public
  servers. Follow Plutonium's rules.

Things that were tried and left out

- A comic-book color look using the game's color settings: no visible
  effect in this game.
- Team color markers over players: dropped because of lag.
- A script that swaps the team emblem to a different picture: dropped
  because of blank squares.

------------------------------------------------------------------------

Uninstall

Delete the mod's files from scripts\mp and images, and delete
z_vghs_menu.iwd if you added the wallpaper. If you changed the intro
video, put your backup of the original file back in the video folder, or
let Plutonium restore it. Then fully restart the game. Nothing else was
changed. You can leave Bot Warfare in place or remove z_svr_bots.iwd the
same way.

------------------------------------------------------------------------

Credits and disclaimer

Bot Warfare: https://github.com/ineedbots/iw4_bot_warfare
Plutonium: https://plutonium.pw/
VGHS Show: https://www.youtube.com/@rocketjump
Video Game High School

This mod is a fan tribute to Video Game High School (VGHS), the web
series from RocketJump, created by Freddie Wong, Matthew Arnold, Will
Campos and Brian Firenzi, and made with its cast and crew.

All credit goes to them for:

- the Video Game High School name and logo, used here for the team
  emblems and the on-screen logos
- the school, team and game names taken from or inspired by the show,
  such as "Field of Fire" and the rival school team names
- the look, setting and world that the mod is based on

The logo, names and likeness of Video Game High School belong to
RocketJump and the show's creators. They are used here only as a
non-commercial fan tribute, and this mod is not affiliated with or
endorsed by them. If you are a rights holder and want something changed
or removed, please contact [your contact here], and it will be taken
down.

If you like the mod, watch the show. The series was released on
RocketJump's website and YouTube.

Everything else

- Mod by: your name here
- Built on Plutonium and Bot Warfare. See their pages for their credits.
- Call of Duty and Modern Warfare belong to Activision.
- This mod contains no game files. Use it only with your own legitimate
  copy of MW3.
